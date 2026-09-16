# Stages

> **Dominio 3** · Carga por archivos

Un **stage** es un **puntero a una ubicación donde viven archivos**, listos para cargarse a una tabla (o donde Snowflake deja los archivos al descargar). No es la tabla: es el "buzón" intermedio [...]

> **💡 PIÉNSALO ASÍ:** El stage es la **zona de recepción** de un almacén. Los archivos llegan ahí; `COPY INTO` los mete a la estantería (la tabla).

## Dos grandes tipos
- **Internos** — el almacenamiento lo gestiona Snowflake. Ver [internal-stages.md](./internal-stages.md).
- **Externos** — apuntan a tu bucket en S3 / Azure / GCS. Ver [external-stages.md](./external-stages.md).

## Notación `@`
| Referencia | Qué es |
|---|---|
| `@~` | Stage del **usuario** (interno) |
| `@%mi_tabla` | Stage de **tabla** (interno) |
| `@mi_stage` | Stage **con nombre** (interno o externo) |

## Subir y bajar archivos
- **`PUT`** sube archivos locales a un stage **interno** (desde SnowSQL / Snowflake CLI).
- **`GET`** descarga archivos de un stage interno a tu máquina.
- A un stage **externo** los archivos llegan por tu proveedor de nube o tu pipeline; Snowflake solo los **lee**.

## Extras útiles
- Un stage puede tener un **file format** asociado ([file-formats.md](./file-formats.md)).
- Un stage puede tener una **directory table** (catálogo de archivos) para datos no estructurados (PDFs, imágenes).
- `LIST @mi_stage` lista los archivos del stage.

> **✅ REGLA RÁPIDA:** Stage = puntero a archivos. `PUT`/`GET` solo con stages **internos**. Para externos, usa una [storage integration](./storage-integrations.md) y deja que la nube deposite l[...])

## Ver también
- [copy-into.md](./copy-into.md) · [internal-stages.md](./internal-stages.md) · [external-stages.md](./external-stages.md)
