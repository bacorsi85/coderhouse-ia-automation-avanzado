# `traceId` en n8n: lo implementado en el M8

**Dónde:** el manager `checkpoint8_bruno_acorsi` (`jl7pW9jx9CrbRvYV`), copia del M4 con el supervisor del M8, sus workers (sub-workflows de los especialistas) y el sub-workflow `supervisor_juez_m8_acorsi_bruno`. Registro en la Data Table de n8n `qa_juez_m8` (`x44UcLY8HmbL7wg2`).
**Estado:** implementado. El `trace_id` se genera en el manager **antes de delegar**, viaja como input al worker, vuelve en el contrato del worker, pasa al supervisor y queda en cada fila de `qa_juez_m8` y en el mensaje de Slack. Las 10 corridas A/B y las demos del 12-10-2026 (evidencia en `m8/evidencia-ab/` y `m8/resultados-m8.md`) se hicieron con la versión anterior, que generaba el id en *M8 · Preparar evaluación*, después de la respuesta del worker. El formato es el mismo en las dos versiones.
**Nombre del campo:** en n8n es `trace_id`. En el informe M9 se lo llama `traceId`, el nombre de la consigna: es el mismo dato.

---

## 1. Dónde se genera

En el nodo Code **`M8 · Generar traceId`** del manager, que corre **antes de `Delegar a worker`**:

```js
trace_id = 'pt-' + $execution.id + '-' + Date.now().toString(36)
```

- **Formato:** `pt-<executionId>-<base36>`. Ejemplo real: `pt-403-mv4nolag` (caso C1, variante B, generado con la versión anterior).
- **Por qué así:** `$execution.id` apunta directo a la ejecución del padre en *Executions* (`pt-403-…` → ejecución 403). El sufijo es `Date.now()` en base 36: lo hace único aunque la misma ejecución se evalúe más de una vez, y no depende de que el nodo Code permita `crypto`.
- **Por qué antes de delegar:** así el worker ya lo recibe, y su sub-ejecución queda atada al mismo id que el resto del caso.
- Se genera **una sola vez por caso**: todo lo que viene después lo recibe, no lo vuelve a calcular.

## 2. Por dónde viaja

| Paso | Nodo | Qué pasa con el `trace_id` |
|---|---|---|
| 1 | `M8 · Generar traceId` (manager) | Se genera, antes de delegar |
| 2 | `Delegar a worker` (Execute Workflow, manager) | Lo pasa como input al sub-workflow del especialista, junto con la consulta |
| 3 | Worker (especialista) | Lo devuelve en su contrato de salida: `{status, worker, respuesta, requires_human, error, trace_id}` |
| 4 | `Consolidar resultado` y `M8 · Preparar evaluación` (manager) | Toman el `trace_id` del contrato y lo meten en el payload del supervisor |
| 5 | `M8 · Supervisor (Juez)` (Execute Workflow, manager) | Lo pasa como input al sub-workflow `supervisor_juez_m8_acorsi_bruno` (`waitForSubWorkflow: true`) |
| 6 | Supervisor: registro en `qa_juez_m8` | Se escribe en **cada fila**: una por veredicto, incluidos los intermedios. La columna `intento` (0, 1, 2) distingue los reintentos de autocorrección; en un CORREGIR el supervisor re-delega al mismo worker con la crítica y el mismo `trace_id` |
| 7 | Supervisor: mensaje de Slack de revisión humana | Aparece en el mensaje a `#operaciones` con Aprobar / Editar (demo RECHAZADO, ejecución 452) |
| 8 | `M8 · Resultado final` (manager) | Vuelve al manager en el contrato de salida, junto con `estado_veredicto`, `exactitud_factual` y `decision_humana` |
| 9 | Respuesta al cliente | **No va**: el `trace_id` no se le muestra al cliente |

## 3. El registro: Data Table `qa_juez_m8`

Columnas: `id_evaluacion, trace_id, timestamp, execution_id, caso_id, arquitectura, session_id, intent, worker, intento, query_original, contexto_resumen, respuesta_agente, exactitud_factual, estado_veredicto_llm, estado_veredicto, motivo_codigo, categoria_error, critica, modelo_agente, modelo_juez, decision_humana, respuesta_final, timestamp_decision`.

- `id_evaluacion` = `<execution_id>-<intento>` (por ejemplo `441-0` y `441-1` en la demo de autocorrección). Es la clave para actualizar la fila con la decisión humana.
- `confidenceScore` del esquema de la consigna: el Juez no devuelve un campo de confianza, así que se usa `exactitud_factual ÷ 5`.
- Captura de la tabla con la columna `trace_id`: `capturas/d1-qa-juez-traceid.jpg` (12 filas del 12-10-2026).

## 4. Fila de ejemplo (real)

Ejecución 403, caso C1 en la variante B:

```json
{
  "trace_id": "pt-403-mv4nolag",
  "timestamp": "2026-10-12T02:51:46.960Z",
  "execution_id": "403",
  "caso_id": "C1",
  "arquitectura": "B",
  "intent": "SALES",
  "worker": "worker3_sales_modulo8B_acorsi_bruno",
  "intento": 0,
  "exactitud_factual": 5,
  "estado_veredicto": "ACEPTADO",
  "categoria_error": "NINGUNO",
  "modelo_juez": "gpt-4.1-mini",
  "decision_humana": "AUTOMATICA"
}
```

Costo medido de esa ejecución: USD 0,002166 (4 llamadas LLM, 7.986 / 289 tokens). No es una columna de la tabla: sale del `tokenUsage` de cada nodo de modelo.

## 5. Cómo comprobarlo

1. Correr una consulta por el *Banco de pruebas M8* (o un email) y anotar el número de ejecución del manager.
2. **Esperado:** la salida de *M8 · Generar traceId* trae `trace_id = pt-<ese número>-…`; el mismo valor aparece en el input y en el contrato de salida de la sub-ejecución del worker, en `qa_juez_m8` (una fila o más, si hubo reintentos), en la salida de *M8 · Resultado final* y, si el caso fue a revisión humana, en el mensaje de `#operaciones`. En la respuesta al cliente no aparece.
3. Filtrar `qa_juez_m8` por ese `trace_id`: las filas quedan ordenadas por `intento`.

## 6. Mejora futura

Queda pendiente extender la traza a un registro por nodo: escribir el `trace_id` también en el log de Sheets del padre (*Log de trazabilidad*) y registrar una fila por nodo, con `systemPromptSnapshot` (versión y hash del prompt), en una pestaña `Trazas`.
