# Conector de Kafka

> **Dominio 3** · Ingesta continua

El **Snowflake Connector for Kafka** consume mensajes de **topics de Kafka** y los carga en tablas: **cada topic → una tabla**.

## Cómo funciona
- Por debajo usa **Snowpipe** (modo archivos) o **[Snowpipe Streaming](./snowpipe-streaming.md)** (modo baja latencia).
- En modo Snowpipe, el conector **crea automáticamente** un stage interno y un pipe.
- Por defecto, cada fila cargada tiene dos columnas **VARIANT**: **`RECORD_CONTENT`** (el mensaje) y **`RECORD_METADATA`** (topic, partición, offset, timestamp...).

> **💡 PIÉNSALO ASÍ:** Es un **traductor** entre el mundo Kafka y las tablas de Snowflake: se suscribe a los topics y va depositando cada mensaje como una fila.

## Puntos clave
- Necesita **privilegios** para crear/usar tabla, stage y pipe en el esquema destino (o que ya existan).
- Elegir **Snowpipe vs Snowpipe Streaming** depende de la latencia que necesites.

> **⚠️ TRAMPA DE EXAMEN:** **Cada topic mapea a una tabla**, y en modo archivos el conector **crea el stage y el pipe por ti**. Las columnas por defecto son `RECORD_CONTENT` y `RECORD_METADATA`.

> **✅ REGLA RÁPIDA:** ¿Datos vienen de Kafka? → conector de Kafka (Snowpipe o Snowpipe Streaming por debajo).

## Ver también
- [snowpipe.md](./snowpipe.md) · [snowpipe-streaming.md](./snowpipe-streaming.md) · [connectors.md](./connectors.md)
