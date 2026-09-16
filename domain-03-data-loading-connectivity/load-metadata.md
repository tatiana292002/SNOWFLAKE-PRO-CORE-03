# Load Metadata (metadatos de carga)

> **Dominio 3** · Carga por archivos

Snowflake **recuerda qué archivos ya cargó** en cada tabla para **evitar cargarlos dos veces**.

> **💡 PIÉNSALO ASÍ:** Es una **lista de asistencia**. Si un archivo ya "firmó" (se cargó), no lo vuelve a meter aunque lo intentes de nuevo.

## Cómo funciona
- La metadata de carga se guarda por tabla y dura **64 días**.
- Guarda el **nombre del archivo** y un hash/ETag; si el archivo no cambió, `COPY INTO` lo **salta**.
- **`FORCE = TRUE`** ignora la metadata y **recarga** todo.
- Pasados los **64 días**, un archivo que siga en el stage **podría recargarse**.

## Dónde consultarla
- `INFORMATION_SCHEMA.COPY_HISTORY` / `LOAD_HISTORY` (tiempo real, por base de datos).
- `SNOWFLAKE.ACCOUNT_USAGE.COPY_HISTORY` (histórico de cuenta).

> **⚠️ TRAMPA DE EXAMEN:** La ventana es de **64 días**. Si quieres reprocesar archivos ya cargados, `FORCE=TRUE` es la palanca (pero cuidado con duplicados).

> **✅ REGLA RÁPIDA:** COPY no recarga archivos ya cargados (64 días); `FORCE=TRUE` obliga; `PURGE=TRUE` los borra del stage tras cargar.

## Ver también
- [copy-into.md](./copy-into.md) · [snowpipe.md](./snowpipe.md)
