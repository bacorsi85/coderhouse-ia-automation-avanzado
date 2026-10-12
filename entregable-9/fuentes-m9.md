# Fuentes del informe M9: precios y políticas

Todas las consultas son del **11-10-2026**, salvo los precios de Anthropic, revisados de nuevo el **12-10-2026** (ver P10–P13). Los precios están en USD salvo que se indique otra moneda. "Oficial" quiere decir la página del propio proveedor; "secundaria" es una fuente de terceros, que se usa solo donde la oficial no mostraba el dato.

## Precios

| # | Proveedor | Ítem | Valor citado | Fuente (URL) | Tipo |
|---|---|---|---|---|---|
| P1 | Groq | `qwen/qwen3.8-27b` | USD 0,80 entrada / 4,00 salida por millón de tokens. Figura en **Preview Models**: "evaluation only", no para producción | https://console.groq.com/docs/models | Oficial |
| P2 | Groq | `openai/gpt-oss-120b` | USD 0,15 / 0,60 por millón | https://console.groq.com/docs/models | Oficial |
| P3 | Groq | `openai/gpt-oss-20b` | USD 0,075 / 0,30 por millón | https://console.groq.com/docs/models | Oficial |
| P4 | Groq | `whisper-large-v3` / `-turbo` | USD 0,111 / 0,04 por hora de audio | https://console.groq.com/docs/models | Oficial |
| P5 | Groq | `llama-3.3-70b-versatile` | Sin precio público ("Contact Sales"). Coincide con el "resource not found" del M4 | https://console.groq.com/docs/models | Oficial |
| P6 | Groq | Límites base | qwen3.8-27b, gpt-oss-120b y gpt-oss-20b: 30 pedidos/min, 1.000 pedidos/día, 8.000 tokens/min y 200.000 tokens/día. La página los presenta como "base limits for the Developer plan" | https://console.groq.com/docs/rate-limits | Oficial |
| P7 | OpenAI | `gpt-4o` | USD 2,50 entrada / 1,25 entrada cacheada / 10,00 salida por millón | https://developers.openai.com/api/docs/pricing | Oficial |
| P8 | OpenAI | `gpt-4o-mini` | USD 0,15 / 0,075 cacheada / 0,60 por millón | https://developers.openai.com/api/docs/pricing | Oficial |
| P8b | OpenAI | Cómo funciona el caché | Automático, sin configurar, en prefijos de 1.024 tokens o más. El informe además supone tramos de 128 tokens y que el caché se borra tras unos minutos sin uso: **esos dos detalles no se consultaron en esta entrega** | https://platform.openai.com/docs/guides/prompt-caching | **A verificar** |
| P9 | OpenAI | `whisper-1` | USD 0,006 por minuto | https://developers.openai.com/api/docs/pricing | Oficial |
| P10 | Anthropic | Claude Sonnet 5.5 | Entrada USD 2. Escritura de caché: 2,50 (5 min) / 4 (1 h). Lectura de caché: **0,20**. Salida: 10 (por millón). **Corrección del 12-10-2026:** la versión anterior decía 0,10 de lectura; el valor correcto es 0,20 (0,1 × la entrada), confirmado en la referencia de la API de Anthropic (tabla de modelos al 06-10-2026) | https://platform.claude.com/docs/en/about-claude/pricing | Oficial |
| P11 | Anthropic | Claude Haiku 5.5 (prompts ≤ 100.000 tokens) | Entrada USD 0,10. Escritura: 0,125 (5 min) / 0,20 (1 h). Lectura: 0,01. Salida: 0,50 | https://platform.claude.com/docs/en/about-claude/pricing | Oficial |
| P12 | Anthropic | Claude Haiku 4.5 / Sonnet 4.6 (referencia) | Haiku 4.5: 1 / 1,25 / 2 / 0,10 / 5. Sonnet 4.6: 3 / 3,75 / 6 / 0,30 / 15 | https://platform.claude.com/docs/en/about-claude/pricing | Oficial |
| P13 | Anthropic | Multiplicadores y mínimos del caché | Escritura de 5 min = 1,25 × la entrada; escritura de 1 h = 2 ×; lectura = 0,1 × la entrada (excepciones: 0,05 × en Opus 5.5 y 0,025 × en Fable 5.1; **Sonnet 5.5 usa la regla general de 0,1 ×**, corregido el 12-10-2026). Mínimo cacheable: 512 tokens en Sonnet 5.5 y Haiku 5.5. TTL por defecto de 5 min. Hasta 4 breakpoints. Existe caché automático con `cache_control` en el nivel superior del pedido | https://platform.claude.com/docs/en/about-claude/pricing · https://platform.claude.com/docs/en/build-with-claude/prompt-caching | Oficial |
| P14 | ElevenLabs | Texto a voz | Multilingual v2/v3: USD 0,08 cada 1.000 caracteres. Flash/Turbo: 0,04. Planes: Free USD 0 (10.000 car.), Starter USD 6 (75.000), Creator USD 22 (275.000), Pro USD 99 (1.238.000), Scale USD 299, Business USD 990. Precios sin impuestos | https://elevenlabs.io/pricing/api | Oficial |
| P15 | LlamaCloud | Créditos | Free USD 0 con 10.000 créditos. Starter USD 50/mes con 40.000. Pro USD 500 con 400.000. 1.000 créditos = USD 1,25. Parseo "desde 1 crédito" por página. **Los créditos de indexado y recuperación no están publicados en la página** | https://www.llamaindex.ai/pricing | Oficial (incompleta) |
| P16 | n8n Cloud | Planes | Starter **€20/mes** facturado anual, 2.500 ejecuciones. Pro **€50/mes** anual, 10.000 ejecuciones. Business €667/mes anual (self-hosted) | https://n8n.io/pricing/ | Oficial |
| P17 | n8n Cloud | Precio con facturación mensual | Starter €24, Pro €60. **La página oficial no mostraba el valor mensual en el texto**. La conversión a dólares del informe (€24 ≈ USD 27) usa un **tipo de cambio supuesto de €1 = USD 1,125**, no una cotización consultada | https://www.jetadmin.io/blog/n8n-pricing/ · https://connectsafely.ai/articles/n8n-cloud-pricing-guide | **Secundaria: verificar en n8n.io** |
| P18 | n8n | Qué consume ejecuciones | Solo cuentan las ejecuciones de producción. En un sub-workflow, "only the parent (top-level) execution counts". Las manuales, las de error y los polls sin datos no cuentan | https://docs.n8n.io/workflows/executions/ | Oficial |
| P19 | n8n Cloud | Concurrencia | Lo que excede el límite del plan "queue for later processing" (FIFO). **El límite numérico por plan no figura en la página** | https://docs.n8n.io/deploy/use-n8n-cloud/understand-concurrency | Oficial (incompleta) |

## Políticas de datos (entrenamiento y retención)

| # | Proveedor | Política | Valor citado | Fuente (URL) |
|---|---|---|---|---|
| D1 | OpenAI | Entrenamiento | Los datos de la API no se usan para entrenar salvo opt-in explícito | https://developers.openai.com/api/docs/guides/your-data |
| D2 | OpenAI | Retención | Logs de monitoreo de abuso hasta 30 días | https://developers.openai.com/api/docs/guides/your-data |
| D3 | OpenAI | ZDR y Modified Abuse Monitoring | Requiere aprobación previa de OpenAI (vía ventas). Una vez aprobado aparece la pestaña *Data Retention* en Settings → Organization → Data controls, con opción por proyecto. Elegibles, entre otros: `/v1/chat/completions`, `/v1/responses`, `/v1/audio/transcriptions`. No elegibles: files, batches, vector stores, fine-tuning | https://developers.openai.com/api/docs/guides/your-data |
| D4 | Groq | Entrenamiento | Services Agreement §4.2: "Groq is not permitted to use Inputs or Outputs for training or fine-tuning any AI Model Services or other models", salvo permiso del cliente | https://console.groq.com/docs/legal/services-agreement |
| D5 | Groq | Retención y ZDR | No retiene la inferencia por defecto. Puede guardar hasta 30 días para confiabilidad y abuso. Cualquier cliente puede activar ZDR en Data Controls (admin de la organización), lo que desactiva batch y fine-tuning. Los datos quedan en Google Cloud, EE. UU. | https://console.groq.com/docs/your-data · https://console.groq.com/settings/data-controls |
| D6 | Anthropic | Entrenamiento | "By default, we will not use your inputs or outputs from our commercial products" para entrenar | https://privacy.claude.com/en/articles/7996868-is-my-data-used-for-model-training |
| D7 | Anthropic | Retención | El artículo de privacidad dice: inputs y outputs de la API "automatically delete … within 30 days". La documentación técnica dice que el contenido "is not retained by default", salvo en los Covered Models, que exigen 30 días. **Discrepancia entre las dos fuentes: la tiene que resolver legal** | https://privacy.claude.com/en/articles/7996866-how-long-do-you-store-my-organization-s-data · https://platform.claude.com/docs/en/manage-claude/api-and-data-retention |
| D8 | Anthropic | ZDR | Se pide al equipo de ventas y se habilita por organización. El Prompt Caching es elegible (la caché vive en memoria durante el TTL). Batch (29 días) y code execution no son elegibles | https://platform.claude.com/docs/en/manage-claude/api-and-data-retention |

## Límites de gasto

| # | Proveedor | Mecanismo | Valor citado | Fuente (URL) |
|---|---|---|---|---|
| L1 | OpenAI | Tope por proyecto | Project settings → Limits → *Edit spend limit* → *Enforce a hard limit*. Al alcanzarlo: 429 `project_spend_limit_exceeded`. Puede excederse un poco mientras se propaga. Sin el tope duro activado es solo alerta. **No se verificó en esta consulta que las llaves estén atadas a un proyecto** (el artículo de ayuda devolvió 403) | https://developers.openai.com/api/docs/guides/spend-limits |
| L2 | Anthropic | Tope por workspace | Settings → Workspaces → *Spend limits*: tope mensual con alertas por umbral. No se puede fijar en el Default Workspace. Las llaves pueden atarse a un workspace. Se recomienda un workspace por entorno (Development, Staging, Production) | https://platform.claude.com/docs/en/build-with-claude/workspaces |
| L3 | Groq | Tope por organización | Settings → Billing → Limits (plan pago y rol owner). **Es por organización, no por llave ni por proyecto.** Tope duro: 400 `blocked_api_access`, medido con 10–15 min de demora. Las alertas son aparte. Solo hay límite mensual, que se reinicia el día 1 | https://console.groq.com/docs/spend-limits |

## Datos medidos (no son precios publicados)

| # | Dato | Valor | Fuente |
|---|---|---|---|
| M1 | Costo por ejecución, variante B (Router y workers `gpt-4o-mini`, Juez `gpt-4.1-mini`) | USD 0,0018; × 1.000 = USD 1,83 | `m8/resultados-m8.md` (tokens del `tokenUsage` de cada nodo de modelo, 12-10-2026) |
| M2 | Precisión y exactitud del Juez, variante B | 5/5 casos correctos; exactitud media 5,0 en 4 evaluados | `m8/resultados-m8.md` |
| M3 | Latencia media por consulta, variante B | 10,1 s | `m8/resultados-m8.md` |
| M4 | Duración máxima de una ejecución en la instancia de n8n Cloud | 180 s | Error real de la API de n8n, 12-10-2026 |
| M5 | Precio de `gpt-4.1-mini` | USD 0,40 entrada / 1,60 salida por millón | `m8/plan-m8.md` §4.3, consultado el 11-10-2026 |
| M6 | Costo de la hora de soporte | USD 20 por hora (*supuesto*) | Diapositiva de ROI de la clase 8 |
| M7 | Tokens de entrada de la primera llamada de cada worker, variante B | Sales 1.461 · Billing 1.523 · Tech Support 1.977 y 1.986; 2 llamadas al worker en C1–C4, 0 en C5 (1,6 por ejecución) | `tokenUsage` de cada nodo de modelo, ejecuciones 403, 412, 421 y 430 (12-10-2026) |
| M8 | Registro del Juez | 12 filas en `qa_juez_m8`: 10 ACEPTADO, 1 CORREGIR (`TONO_O_FORMATO`), 1 RECHAZADO (`PROMESA_NO_AUTORIZADA`). La fila de la ejecución 403 tiene `timestamp` 2026-10-12T02:51:46.960Z | Data Table `qa_juez_m8` y `m8/capturas/d1-qa-juez-traceid.jpg`, `d2-qa-juez-veredictos.jpg` |

## Lo que no se pudo verificar

- Precio mensual de n8n Cloud en la página oficial (solo aparece el anual). Se usó una fuente secundaria, marcada como tal.
- Tipo de cambio euro / dólar: no se consultó una cotización; se usa €1 = USD 1,125 como supuesto.
- Detalles del caché de OpenAI (tramos de 128 tokens, cuánto dura sin uso) y si OpenAI ya cachea hoy la segunda llamada del worker dentro del mismo caso: el `tokenUsage` de n8n no informa tokens cacheados, así que el costo medido usa el precio de lista y es una cota superior.
- El tamaño de la parte fija de cada worker (≈ 1.300 tokens): es un supuesto a partir de los tokens medidos en la primera llamada, no se contó el prompt.
- Precios de Anthropic: se confirmaron con la referencia de la API de Anthropic (tabla de modelos al 06-10-2026), no con una nueva lectura de la página de precios.
- Límite numérico de concurrencia por plan de n8n Cloud.
- Créditos de LlamaCloud por indexado y por consulta de recuperación. **Ya no hace falta para el informe:** el RAG final usa LlamaCloud solo para parsear el manual en la ingesta (42 créditos por carga del manual de 14 páginas); las preguntas se buscan en n8n con embeddings de OpenAI `text-embedding-3-small` y no consumen créditos.
- Si OpenAI ata cada API key a un proyecto: es lo esperable, pero no se confirmó en esta consulta.
- Si el nodo *Anthropic Chat Model* de n8n expone `cache_control`.
- Prompt caching de Groq (no se consultó).
- Políticas de datos de ElevenLabs y LlamaCloud: quedan como control pendiente (se verifican antes de procesar datos reales).
- Límites de la cuenta de OpenAI (nivel de uso): se verifican en la consola antes de producción.
- Material de la clase 9 de la profe: la carpeta `clase 9` del repo `Carolina053Peke/AI-Automation-Avanzado` solo contiene `clase9.md` con el texto "clase 9" (commit del 09-10-2026). No hay material para alinear. El documento se alineó con la consigna, con el README del repo ("Semana 9: deployment, monitoreo y alertas, cost optimization") y con la diapositiva 4 de la clase 8 (ROI y TCO).
