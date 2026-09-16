# Snowpipe ⭐

> **Dominio 3** · Ingesta continua

Servicio de **carga continua y serverless** que ingiere archivos **en cuanto llegan** al stage, en micro-lotes.

## Cómo funciona
- Se define un **pipe**: `CREATE PIPE ... AS COPY INTO ...`.
- Con **`AUTO_INGEST = TRUE`** se dispara solo con **notificaciones de eventos** de la nube (SQS/SNS, Event Grid, Pub/Sub). Alternativa: la **REST API** (`insertFiles`).
- Es **serverless**: **no usa tu warehouse**; Snowflake pone el cómputo y se **factura aparte** (cómputo por segundo + un pequeño overhead por archivo, ~0.06 créditos / 1000 archivos).

> **💡 PIÉNSALO ASÍ:** Snowpipe es una **cinta transportadora** siempre encendida: apenas cae un archivo en el buzón, lo mete a la tabla, sin que tú prendas una cocina (warehouse).

## Buenas prácticas
- Tamaño de archivo ideal **~100–250 MB** comprimido. Evita miles de archivos diminutos (mucho overhead) y archivos gigantes (más latencia).
- Default de **`ON_ERROR = SKIP_FILE`** (distinto del COPY masivo).
- Aplica la **metadata de carga** para no duplicar (ver [load-metadata.md](./load-metadata.md)).

## Snowpipe vs COPY masivo
| | COPY (bulk) | Snowpipe |
|---|---|---|
| Disparo | Manual / programado | Automático al llegar el archivo |
| Cómputo | **Tu warehouse** | **Serverless** (aparte) |
| Caso | Lote grande puntual | Archivos que llegan seguido |

> **⚠️ TRAMPA DE EXAMEN:** Snowpipe **no usa un warehouse** del usuario y se factura por separado. Su latencia es de **~minutos**, no tiempo real de verdad (para eso, Snowpipe Streaming).

> **✅ REGLA RÁPIDA:** ¿Archivos que llegan continuamente y quieres cargarlos solos, sin warehouse? → **Snowpipe**.

## Ver también
- [snowpipe-streaming.md](./snowpipe-streaming.md) · [copy-into.md](./copy-into.md) · [kafka.md](./kafka.md)
