# Snowpipe Streaming

> **Dominio 3** · Ingesta continua

Ingesta de datos **fila por fila** (no por archivos), con **latencia más baja** que Snowpipe clásico. Escribe las filas **directamente** en la tabla mediante un **SDK** (cliente), sin pasar por u[...])

> **💡 PIÉNSALO ASÍ:** Si Snowpipe es una cinta que mueve **cajas** (archivos), Snowpipe Streaming es una **tubería** que mete **gota a gota** (filas) directo al tanque.

## Puntos clave
- **Sin archivos, sin stage**: la aplicación escribe filas a través de **canales** (channels) con el SDK.
- **Menor latencia y menor costo** para cargas de streaming continuo.
- Es el modo que usa el **[conector de Kafka](./kafka.md)** en su variante de baja latencia.

## Snowpipe vs Snowpipe Streaming
| | Snowpipe (clásico) | Snowpipe Streaming |
|---|---|---|
| Unidad | **Archivos** en un stage | **Filas** directas |
| Latencia | Minutos | Segundos / sub-segundo |
| Mejor para | Archivos que caen seguido | Streams en vivo (IoT, eventos) |

> **⚠️ TRAMPA DE EXAMEN:** Streaming **no usa stage ni archivos**. Si el caso dice "filas en vivo, mínima latencia" → Snowpipe **Streaming**; si dice "archivos que llegan continuamente" →[...])

> **✅ REGLA RÁPIDA:** Streaming = filas directas, baja latencia, base del modo rápido de Kafka.

## Ver también
- [snowpipe.md](./snowpipe.md) · [kafka.md](./kafka.md)
