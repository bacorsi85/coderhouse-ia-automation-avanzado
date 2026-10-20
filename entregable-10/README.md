# Entregable 10 — Brochure técnico-comercial

**Pre-entrega del Módulo 10.** Archivo de entrega:
[`PreEntrega_Modulo10_BrunoAcorsi.pdf`](PreEntrega_Modulo10_BrunoAcorsi.pdf). Fuente: [`brochure-m10.html`](brochure-m10.html).

| Archivo | Qué es |
|---|---|
| `PreEntrega_Modulo10_BrunoAcorsi.pdf` | La entrega (7 páginas): narrativa ejecutiva y arquitectura de valor · Función → Beneficio · business case del M9 sin recalcular · roadmap por fases 0–3 con fallback · pricing híbrido (setup + retainer + success fee) con KPI atribuible y ventana de conversión · plan a 30 días con responsables por rol · metadatos en el CRM · tres objeciones |
| `brochure-m10.html` | Fuente del PDF (se imprime con Edge headless) |

Está escrito para un comité de negocio: no usa jerga técnica ni capturas del editor. El diagrama muestra
el coordinador, los especialistas, el supervisor de calidad y las herramientas como un equipo de soporte.

## De dónde sale cada número

| Dato | Origen |
|---|---|
| Ahorro USD 550/mes, payback 2,2 meses, año 1 USD 5.400, peor mes USD 418, 3 escenarios | Business case del [entregable 9](../entregable-9/informe-m9.md), sin recalcular |
| Setup USD 1.200 · retainer USD 400 · success fee USD 0,30 por consulta (tope USD 300/mes) | Modelo híbrido del entregable 9 (clase 10) |
| Semáforo verde / amarillo / rojo y escenario de volumen | [Entregable 7](../entregable-7/) (escenario supuesto, rotulado) |
| 5/5 respuestas con el manual, "No sé" y derivación | [Entregable 5](../entregable-5/) |
| Supervisor de calidad: 5/5 con nota 5 y el reembolso frenado (nota 2) que corrigió una persona | [Entregable 8](../entregable-8/) |
| Código de seguimiento de punta a punta | `trace_id` de los entregables 8 y 9 |

## Supuestos de esta entrega

- **Ventana de conversión de 3 días corridos:** una consulta se factura si en los 3 días posteriores a la
  última respuesta el local no vuelve por el mismo tema ni pide una persona.
- **Plan a 30 días** con inicio supuesto el lunes 26 de octubre de 2026.
- **Metadatos en HubSpot** como actividad por caso en la ficha del local; las propiedades se crean en el hito 4.
- Los controles de presupuesto con tope, el tope de 10 mensajes por conversación y la rama de error que
  deriva a una persona están **diseñados** (entregable 9) y se construyen en la implementación.
