# Dominio 3 — Data Loading, Unloading & Connectivity

> **Peso en el examen: ~18%** · Guía de estudio SnowPro Core COF-C03 (formato "explicado fácil")

Este dominio cubre cómo **entran y salen los datos** de Snowflake y **cómo te conectas** a la plataforma. Se organiza en tres bloques:

1. **Carga y descarga por archivos** — stages, `COPY INTO`, formatos, metadatos de carga y validación.
2. **Ingesta continua / automática** — Snowpipe, Snowpipe Streaming, conector de Kafka, Openflow.
3. **Conectividad** — drivers, connectors e integraciones (storage / API / Git) y la CLI de Snowflake.

## 📁 Contenido

### Stages y carga por archivos
- [stages.md](./stages.md) — qué es un stage y sus tipos
- [internal-stages.md](./internal-stages.md) — stages internos (user, table, named)
- [external-stages.md](./external-stages.md) — stages externos (S3 / Azure / GCS)
- [storage-integrations.md](./storage-integrations.md) — credenciales seguras hacia la nube
- [copy-into.md](./copy-into.md) — el comando de carga/descarga ⭐
- [file-formats.md](./file-formats.md) — CSV, JSON, Parquet, etc.
- [load-metadata.md](./load-metadata.md) — cómo Snowflake evita duplicados
- [validation-mode.md](./validation-mode.md) — validar sin cargar

### Ingesta continua
- [snowpipe.md](./snowpipe.md) — carga continua serverless ⭐
- [snowpipe-streaming.md](./snowpipe-streaming.md) — ingesta fila por fila
- [kafka.md](./kafka.md) — conector de Kafka
- [openflow.md](./openflow.md) — integración de datos (no evaluado hasta GA)

### Conectividad
- [drivers.md](./drivers.md) — JDBC, ODBC, Python...
- [connectors.md](./connectors.md) — integraciones con herramientas
- [api-integrations.md](./api-integrations.md) — llamar servicios externos
- [git-integrations.md](./git-integrations.md) — versionar y desplegar desde Git
- [snowflake-cli.md](./snowflake-cli.md) — la CLI moderna

## 🎯 Cómo estudiar este dominio
- Lo que MÁS cae: `COPY INTO` (opciones y sintaxis), la diferencia **carga masiva (COPY) vs continua (Snowpipe) vs streaming**, y **no confundir las tres integrations** (storage / API / Git).
- `openflow.md` y el warehouse por defecto de Notebooks: **solo reconocerlos**, no entran en detalle (no evaluados hasta GA).

## 🏷️ Convención de recuadros
- **💡 PIÉNSALO ASÍ** — analogía para entenderlo
- **⚠️ TRAMPA DE EXAMEN** — dónde te intentan enredar
- **✅ REGLA RÁPIDA** — lo que debes recordar sí o sí
- **🆕 NUEVO** — añadido del temario 2026
