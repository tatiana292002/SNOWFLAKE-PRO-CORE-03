# Snowflake Cortex

## Overview

La guía agrupa las capacidades de Cortex en familias.

## LLM / Language Functions

Funciones indicadas:

- `COMPLETE`
- `SUMMARIZE`
- `TRANSLATE`
- `SENTIMENT`
- `EXTRACT_ANSWER`
- `EMBED_TEXT`

Usos principales:

| Function | Purpose |
|---|---|
| `COMPLETE` | Generar texto / interacción con LLM |
| `SUMMARIZE` | Resumir |
| `TRANSLATE` | Traducir |
| `SENTIMENT` | Analizar sentimiento |
| `EXTRACT_ANSWER` | Responder a partir de texto |
| `EMBED_TEXT` | Generar embeddings |

## Document AI / PARSE_DOCUMENT

La guía lo relaciona con extracción de texto y datos estructurados desde:

- PDFs;
- documentos.

## Classical ML

Funciones indicadas:

- `FORECAST`
- `ANOMALY_DETECTION`
- `CLASSIFICATION`

Usos:

- pronóstico de series temporales;
- detección de anomalías;
- clasificación.

## Cortex Search

Servicio de búsqueda **semántica/híbrida** sobre datos propios, especialmente texto y documentos.

La guía lo relaciona con casos de búsqueda tipo buscador inteligente o retrieval para sistemas RAG.

## Cortex Analyst

Permite hacer preguntas en lenguaje natural sobre tablas.

Cortex genera y ejecuta el SQL correspondiente y devuelve la respuesta.

## Quick Rule

```text
Buscar dentro de documentos/texto propio
→ Cortex Search

Preguntar en lenguaje natural sobre tablas
→ Cortex Analyst

Generar / resumir / traducir texto
→ LLM functions
```

## Exam Focus

La distinción Search vs Analyst es especialmente importante.

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
