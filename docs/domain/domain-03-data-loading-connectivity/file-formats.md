# File Formats

> **Dominio 3** · Carga por archivos

Definen **cómo interpretar** los archivos que cargas o descargas. Se pueden escribir **en línea** dentro del `COPY INTO` o guardarse como un **objeto file format** reutilizable.

## Formatos soportados
| Formato | Tipo | Nota |
|---|---|---|
| **CSV** (delimitado) | Estructurado | Opciones como `FIELD_DELIMITER`, `SKIP_HEADER`, `FIELD_OPTIONALLY_ENCLOSED_BY` |
| **JSON** | Semiestructurado | Se carga en una columna **VARIANT** |
| **AVRO**, **ORC**, **PARQUET** | Semiestructurado | Formatos columnar/binarios; también a VARIANT |
| **XML** | Semiestructurado | A VARIANT |

> **💡 PIÉNSALO ASÍ:** El file format es la **"receta de lectura"**: le dice a Snowflake dónde termina cada campo, si hay encabezado, cómo están las comillas, etc.

## Detalles de examen
- Los **semiestructurados** (JSON, Avro, Parquet, ORC, XML) se cargan típicamente en una columna **VARIANT** y luego se navegan con `:`, `.`, `[n]` y `FLATTEN`.
- Para JSON con un array externo grande: **`STRIP_OUTER_ARRAY = TRUE`** parte el array en **una fila por elemento**.
- Snowflake **autodetecta la compresión** (gzip, bzip2, zstd...) en la mayoría de casos.

> **⚠️ TRAMPA DE EXAMEN:** Un **file format como objeto** se puede reutilizar y otorgar; los **table stages no admiten file format propio** (ver [internal-stages.md](./internal-stages.md)).

> **✅ REGLA RÁPIDA:** CSV = estructurado; JSON/Avro/Parquet/ORC/XML = semiestructurado → VARIANT.

## Ver también
- [copy-into.md](./copy-into.md) · [stages.md](./stages.md)
