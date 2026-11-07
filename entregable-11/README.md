# Entregable 11 — Proyecto Final Integrador: sistema agéntico empresarial

**Proyecto final del curso.** Archivo de entrega (DMSA):
[`Acorsi_Bruno_ProyectoFinal_AI_Experto.pdf`](Acorsi_Bruno_ProyectoFinal_AI_Experto.pdf), de 8 páginas: portada y resumen ejecutivo ·
arquitectura (diagrama Manager-Worker con `traceId`, recorrido con tiempos, memoria persistente, robustez y
capturas del lienzo) · reporte de auditoría (rúbrica, umbral y 3 veredictos reales en JSON) · ROI con tokens
medidos · anexo técnico (tablas, variables y parámetros, sin valores secretos).

El sistema ensambla las pre-entregas en **once sub-workflows independientes** de n8n (carpeta M11), todos
exportados en esta carpeta, **sin credenciales**: n8n solo exporta el nombre y el id de cada credencial.

| Workflow | Rol |
|---|---|
| `pf_00_ingreso_acorsi_bruno` | Webhook `POST /webhook/protable-soporte`: valida, calcula la clave de idempotencia (SHA-256), crea el `traceId`, responde **202** al instante y llama al manager **sin esperar**. Repetido → **200 "duplicado"**; inválido → **400** |
| `pf_10_manager_acorsi_bruno` | Manager: memoria → router → especialista → supervisor → (solo si aprueba) CRM y despacho. Ramas de error → estado `ERROR` + alerta con `traceId` |
| `pf_11_memoria_acorsi_bruno` | Memoria de largo plazo por local (`session_id` = email): historial y resumen cada 5 mensajes |
| `pf_21/22/23_worker_*_acorsi_bruno` | Workers Billing, Tech Support y Sales (copias del M8, variante B, `gpt-4o-mini`) |
| `pf_25_rag_manual_acorsi_bruno` | Búsqueda en el manual del M5 (Top-K 4, Minimum Score 0,40) |
| `pf_30_supervisor_juez_acorsi_bruno` | AI-as-a-Judge (copia del M8): `exactitud_factual` < 4 no se libera; reintento; Aprobar / Editar en Slack |
| `pf_40_crm_hubspot_acorsi_bruno` | HubSpot: contacto (crear o actualizar por email) + tarea con `traceId`; idempotente con `crm_ok` |
| `pf_50_despacho_acorsi_bruno` | Slack `#operaciones` + borrador en Gmail; cada envío una sola vez (`slack_ok`, `gmail_ok`) |
| `pf_90_alertas_acorsi_bruno` | Error Trigger de todos los anteriores: alerta en Slack y, si falla, por email |

Tablas (Data Tables de n8n): `pf_solicitudes`, `pf_memoria`, `pf_qa_juez` y `rag_manual_protable_m5` (solo lectura).
Las columnas están en el anexo del PDF.

## Pruebas reales, con el texto exacto de cada consulta

Todas se mandaron al webhook publicado con `{"email", "nombre", "asunto", "mensaje"}` (emails de prueba).

| # | Caso | Consulta exacta | Resultado | `traceId` |
|---|---|---|---|---|
| 1 | Con cobertura | Asunto "Precio del plan Pro": *"Hola, tengo un bar con 20 mesas. ¿Cuánto sale el plan Pro por mes y tiene período de prueba?"* | 202 en 2,6 s · Juez 5/5 ACEPTADO · COMPLETADO en 21 s (HubSpot, Slack, Gmail) | `pf-20261102-122914-1c679e` |
| 2 | Sin cobertura ("No sé") | Asunto "Horario de soporte": *"¿En qué horario atiende el soporte telefónico y cuál es el tiempo máximo de respuesta garantizado (SLA)?"* | "No sé" literal, sin inventar · Juez 5/5 · COMPLETADO en 11 s | `pf-20261102-122942-8381bf` |
| 3 | Promesa inyectada, decide una persona | Asunto "Me cobraron dos veces": *"Hola, en el resumen de la tarjeta veo dos cobros de la suscripción de noviembre. ¿Cómo lo solucionamos?"* + `"modo_prueba": "RECHAZAR"` | Juez 2/5 RECHAZADO (PROMESA_NO_AUTORIZADA) → Editar en Slack → sale la versión humana · COMPLETADO en 135 s | `pf-20261107-104231-5d66b7` |
| 3b | Promesa inyectada, nadie decide | Asunto "Cobro duplicado": *"Este mes me cobraron dos veces la suscripción en la tarjeta. ¿Qué tengo que hacer?"* + `"modo_prueba": "RECHAZAR"` | Juez 2/5 · vencieron los 30 min → `SIN_DECISION_HUMANA`, no sale nada | `pf-20261102-123157-55c00c` |
| 4 | Mismo POST repetido | El del caso 1, otra vez | 200 "duplicado" con el mismo `traceId`, sin reprocesar | `pf-20261102-122914-1c679e` |
| 5 | Email inválido | `{"email": "no-es-email", "mensaje": "hola"}` | 400 "email inválido" en 0,5 s | — |
| 6 | Reproceso de un caso completado | CRM y despacho del caso 1, de nuevo (ejecuciones de prueba 737 y 738) | "omitido: ya registrado / ya enviado / ya creado" | `pf-20261102-122914-1c679e` |
| 7 | Caída de una API externa | Flujo descartable que simula "HubSpot respondió 503" | Alerta en Slack en < 1 s con paso, error y ejecución (ejecución 716) | — |
| 8 | Con cobertura, tras ordenar el lienzo | Asunto "Mercado Pago": *"¿Cómo conecto mi cuenta de Mercado Pago para cobrar los pedidos por QR?"* | Juez 5/5 ACEPTADO · COMPLETADO en 20 s | `pf-20261107-111525-153d2a` |

`modo_prueba = "RECHAZAR"` es una inyección de falla controlada: agrega a la respuesta una promesa de devolución
y descuento para auditar que el supervisor la frena. Cualquier otro valor se ignora.

## De dónde sale cada número del ROI

| Dato | Origen |
|---|---|
| 7.852 / 263 tokens y USD 0,00205 por mensaje | `tokenUsage` de cada llamada del caso 1 (el caso 2 dio 7.917 / 288, USD 0,00204). Precios: GPT-4o-mini USD 0,15 / 0,60 y GPT-4.1-mini USD 0,40 / 1,60 por millón (fuentes del [entregable 9](../entregable-9/fuentes-m9.md)) |
| 3 mensajes por consulta, sueldos, dólar $1.535, setup, retainer y success fee | Business case del [entregable 9](../entregable-9/informe-m9.md) |
| Ahorro USD 574/mes y setup en 2,1 meses | Mismo cálculo del M9, con la infraestructura de este sistema (sin voz: tokens medidos + n8n Pro) |
| Volumen y tiempos actuales (10 h fuera de horario, 6 de cada 10 repetidas) | Escenario de trabajo de los entregables 7 y 9 (rotulado) |
