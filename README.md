# Entrega Final — Ecosistema de Automatización con IA

Sistema que recibe consultas de clientes por Gmail, genera una primera respuesta con IA (Google Gemini vía n8n) y espera aprobación humana antes de enviarla. Los casos aprobados quedan registrados en Airtable.

## Contenido del repositorio

| Archivo | Qué es |
|---|---|
| `Documentacion_Entrega_Final.pdf` | Diagrama de arquitectura + estructuras de datos (Airtable/JSON) + matriz de costos + seguridad y resiliencia |
| `My workflow.json` | Blueprint del flujo exportado desde n8n |
| `capatura_Worflow_funcional.PNG` | Captura del flujo funcionando en n8n |
| `Captura_muestras re.PNG` | Captura del mail de aprobación (Human-in-the-loop) |
| `Captura_uso_air.PNG` | Captura de la base en Airtable |

## Links

- **Base de datos (solo lectura):** PEGAR_ACA_EL_LINK_DE_AIRTABLE
- **Dashboard de control (Shared View, KPIs y estado de consultas):** PEGAR_ACA_EL_LINK_DE_LA_VISTA_COMPARTIDA

## Caso de uso

Triage de consultas/reclamos de clientes por email: Gmail Trigger → AI Agent (Gemini + memoria por hilo) → aprobación humana (Send & Wait) → según la decisión, registro en Airtable o reformulación con AI Agent2 → envío final por Gmail.
