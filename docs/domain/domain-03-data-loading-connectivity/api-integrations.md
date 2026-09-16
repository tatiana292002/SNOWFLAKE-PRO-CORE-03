# API Integrations

> **Dominio 3** · Conectividad

Objeto que permite a Snowflake **llamar servicios/APIs externas de forma controlada** — típicamente para **external functions** (funciones que ejecutan lógica fuera de Snowflake).

## Cómo funciona
- Guarda la configuración y credenciales hacia un **gateway externo** (AWS API Gateway, Azure API Management, GCP), **separadas del código SQL**.
- Se usa junto con una **external function** para invocar un endpoint HTTP externo.

> **💡 PIÉNSALO ASÍ:** Es un **teléfono autorizado**: Snowflake solo puede llamar a los números (endpoints) que la API integration tiene registrados.

> **⚠️ TRAMPA DE EXAMEN:** No la confundas con las otras "integration":
> - **API integration** → llamar **servicios/APIs externas** (external functions).
> - **[Storage integration](./storage-integrations.md)** → credenciales hacia un **bucket**.
> - **[Git integration](./git-integrations.md)** → traer **código de un repo**.

> **✅ REGLA RÁPIDA:** ¿Llamar un servicio HTTP externo desde Snowflake sin exponer credenciales? → **API integration** (+ external function).

## Ver también
- [storage-integrations.md](./storage-integrations.md) · [git-integrations.md](./git-integrations.md)
