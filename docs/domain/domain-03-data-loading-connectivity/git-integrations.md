# Git Integrations 🆕

> **Dominio 3** · Conectividad

Permite conectar Snowflake **directo a un repositorio Git** para **traer y desplegar código versionado**: scripts SQL, proyectos de **Snowpark**, **Native Apps** o **Streamlit**.

## Cómo funciona
- Se crea un objeto de **repositorio Git** en Snowflake (apoyado en una **API integration** + un **secret** para autenticarse al repo).
- Snowflake puede **hacer fetch** del repo y **ejecutar/desplegar** desde ahí (por ejemplo, `EXECUTE IMMEDIATE FROM @repo/...`), sin copiar-pegar SQL manualmente.

> **💡 PIÉNSALO ASÍ:** Conectas Snowflake a tu **repo** como en un pipeline de CI/CD: el código vive versionado en Git y Snowflake lo trae y lo corre.

> **⚠️ TRAMPA DE EXAMEN:** De las tres "integration", esta es la de **código versionado**. Si el caso habla de "definiciones en un repositorio", "versionar" o "desplegar desde Git" → **Git [...])

> **✅ REGLA RÁPIDA:** Git integration = traer y desplegar código desde un repositorio versionado.

## Ver también
- [api-integrations.md](./api-integrations.md) · [snowflake-cli.md](./snowflake-cli.md) · [storage-integrations.md](./storage-integrations.md)
