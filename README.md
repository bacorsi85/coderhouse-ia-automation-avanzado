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
| 2 | M2 · Multi-agente | Manager → workers como sub-workflows | *pendiente* |
| 3 | M3 · Memoria | Contexto por `Session_ID` | *pendiente* |
| 4 | M4 · Integraciones | CRM / Calendario / Workspace vía OAuth2 | *pendiente* |
| 5 | M5 · RAG | Base documental / vector store | *pendiente* |
| 6 | M6 · Voz | STT / TTS | *pendiente* |
| … | … hasta M11 | Proyecto Final Integrador | *pendiente* |

## Cómo usar un entregable

1. En n8n: **Workflows → Import from File** y elegí el `.json` de la carpeta.
2. Reasigná las credenciales propias en cada nodo que las pida. El export guarda solo
   la referencia a la credencial, nunca la clave.
3. Seguí el README de la carpeta para probarlo.
