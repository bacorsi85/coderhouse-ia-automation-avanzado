# Coderhouse — IA & Automatización Avanzada

Entregables del curso de **Bruno Acorsi**. Es un solo proyecto integrador que crece
módulo a módulo: cada entregable parte del workflow de n8n del anterior y le suma
los nodos nuevos.

**Caso de negocio:** agente de triage de soporte L1 para **ProTable**, una plataforma
SaaS de pedidos por menú QR para restaurantes. El agente clasifica la consulta,
resuelve lo que puede con el FAQ oficial y registra un ticket cuando hace falta
seguimiento humano.

## Entregables

| # | Módulo | Qué suma | Carpeta |
|---|---|---|---|
| 1 | M1 · Agente base | Trigger → AI Agent (Tools Agent) + System Prompt + 1 Tool → Log de observabilidad | [`entregable-1/`](entregable-1/) |
| 2 | M2 · Multi-agente | Manager → workers como sub-workflows (contrato de datos, Wait for child, fallback) | [`entregable-2/`](entregable-2/) |
| 3 | M3 · Memoria | Memoria híbrida por `Session_ID` (Google Sheets + corto plazo) y summarization > 5 mensajes | [`entregable-3/`](entregable-3/) |
| 4 | M4 · Integraciones | Gmail + HubSpot + Slack por OAuth2, con anti auto-reply, look up antes de crear, borrador HITL y payload limpio | [`entregable-4/`](entregable-4/) |
| 5 | M5 · RAG | Manual de soporte indexado, búsqueda híbrida (Top-K 4, Minimum Score 0,40), citas de sección y regla "No sé" | [`entregable-5/`](entregable-5/) |
| 6 | M6 · Voz | Nota de voz por Telegram → transcripción → agente → respuesta hablada (ElevenLabs), con contingencias | [`entregable-6/`](entregable-6/) |
| 7 | M7 · Consultoría | Informe de consultoría: relevamiento, priorización, arquitectura multi-agente, KPIs y semáforo HITL | [`entregable-7/`](entregable-7/) |
| 8 | M8 · Supervisor | AI-as-a-Judge con rúbrica JSON, 3 rutas (liberar, reintentar, Slack Aprobar/Editar) y A/B de modelos | [`entregable-8/`](entregable-8/) |
| 9 | M9 · Gobernanza | KPIs, ROI y TCO, business case cliente/proveedor, trazabilidad con `traceId` y ética | [`entregable-9/`](entregable-9/) |
| 10 | M10 · Brochure | Propuesta técnico-comercial: roadmap por fases, pricing híbrido, plan a 30 días y objeciones | [`entregable-10/`](entregable-10/) |
| 11 | M11 · Proyecto final | Sistema asincrónico e idempotente: webhook 202, Manager-Worker en 11 sub-workflows, supervisor obligatorio antes del CRM, alertas y DMSA | [`entregable-11/`](entregable-11/) |

## Cómo usar un entregable

1. En n8n: **Workflows → Import from File** y elegí el `.json` de la carpeta.
2. Reasigná las credenciales propias en cada nodo que las pida. El export guarda solo
   la referencia a la credencial, nunca la clave.
3. Seguí el README de la carpeta para probarlo.
