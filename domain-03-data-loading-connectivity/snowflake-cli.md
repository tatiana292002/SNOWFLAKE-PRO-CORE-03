# Snowflake CLI 🆕

> **Dominio 3** · Conectividad / Herramientas

La **CLI moderna de Snowflake** (comando `snow`): ejecuta SQL, **gestiona objetos**, sube/baja archivos y **despliega proyectos** (Snowpark, Native Apps, Streamlit) desde la terminal. El **temario oficial 2026 la lista como la CLI a conocer**, en lugar de SnowSQL.

> **💡 PIÉNSALO ASÍ:** Es la **navaja suiza de terminal** para trabajar contra Snowflake y automatizar despliegues (CI/CD).

## Snowflake CLI vs SnowSQL
| | Snowflake CLI (`snow`) | SnowSQL |
|---|---|---|
| Rol | Moderna, orientada a proyectos / CI-CD | Cliente clásico de SQL |
| Hace | SQL + gestionar objetos + **desplegar** Snowpark/Native Apps/Streamlit | Ejecutar SQL + `PUT`/`GET` |
| Estado | La **recomendada** por el temario actual | Sigue existiendo y válida para `PUT`/`GET` |

> **⚠️ TRAMPA DE EXAMEN:** Si preguntan por la **CLI moderna recomendada** para desplegar un proyecto Snowpark en un pipeline → **Snowflake CLI**. Si el caso solo menciona `PUT`/`GET` desde terminal, **SnowSQL** sigue siendo válido.

> **✅ REGLA RÁPIDA:** `snow` (Snowflake CLI) = CLI moderna para SQL + objetos + despliegues. SnowSQL = clásica, `PUT`/`GET`.

## Ver también
- [drivers.md](./drivers.md) · [git-integrations.md](./git-integrations.md) · [stages.md](./stages.md)
