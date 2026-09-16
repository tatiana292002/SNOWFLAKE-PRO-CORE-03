# COPY INTO ⭐

> **Dominio 3** · Carga y descarga por archivos — **mucha sintaxis en el examen**

El comando central para **cargar** archivos a tablas y **descargar** (unload) tablas a archivos.

- **Cargar:** `COPY INTO mi_tabla FROM @mi_stage ...`
- **Descargar:** `COPY INTO @mi_stage FROM mi_tabla ...`

## Opciones de carga que debes conocer
| Opción | Para qué |
|---|---|
| `FILE_FORMAT` | Formato de los archivos (CSV, JSON, Parquet...). Ver [file-formats.md](./file-formats.md) |
| `ON_ERROR` | Qué hacer si una fila falla (ver tabla abajo) |
| `PATTERN` / `FILES` | Filtrar qué archivos cargar |
| `MATCH_BY_COLUMN_NAME` | Mapear semiestructurado a columnas por nombre |
| `VALIDATION_MODE` | Probar la carga **sin** insertar. Ver [validation-mode.md](./validation-mode.md) |
| `FORCE = TRUE` | Recargar archivos aunque ya se hayan cargado |
| `PURGE = TRUE` | Borrar los archivos del stage tras cargarlos |
| `SIZE_LIMIT`, `TRUNCATECOLUMNS`, `ENFORCE_LENGTH` | Controlar volumen y longitudes |

### Valores de `ON_ERROR`
| Valor | Efecto |
|---|---|
| `ABORT_STATEMENT` | **Default en COPY masivo.** Aborta toda la carga ante el primer error |
| `CONTINUE` | Carga las filas buenas y **omite solo las filas** con error |
| `SKIP_FILE` | Salta el **archivo completo** si tiene algún error (default en Snowpipe) |
| `SKIP_FILE_n` / `SKIP_FILE_n%` | Salta el archivo si supera n errores (o n% de filas) |

## Transformación durante la carga
Puedes reordenar columnas, castear y aplicar transformaciones simples:

```sql
COPY INTO mi_tabla (col1, col2)
FROM (SELECT $1, $2::int FROM @mi_stage)
FILE_FORMAT = (TYPE = CSV);
```

## Descarga (unload)
- Por defecto **divide en varios archivos** (paralelismo) y **comprime** (gzip).
- `SINGLE = TRUE` (un archivo), `MAX_FILE_SIZE`, `HEADER = TRUE`, `OVERWRITE`, `PARTITION BY`.

> **⚠️ TRAMPA DE EXAMEN:** El default de `ON_ERROR` **cambia**: COPY masivo = `ABORT_STATEMENT`; Snowpipe = `SKIP_FILE`. Y no confundas `CONTINUE` (omite **filas** malas) con `SKIP_FILE` (omit[...])

> **✅ REGLA RÁPIDA:** COPY carga y descarga por archivos. Snowflake **no recarga** archivos ya cargados (ver [load-metadata.md](./load-metadata.md)); usa `FORCE=TRUE` para obligar.

## Ver también
- [file-formats.md](./file-formats.md) · [load-metadata.md](./load-metadata.md) · [validation-mode.md](./validation-mode.md) · [snowpipe.md](./snowpipe.md)
