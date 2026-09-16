# Dynamic Tables

## ¿Qué es?

Una Dynamic Table es una forma declarativa de definir una transformación y el nivel de frescura deseado. Snowflake se encarga de mantener el resultado actualizado.

## Conceptos principales

Una Dynamic Table se define alrededor de:

- Query.
- TARGET_LAG.
- WAREHOUSE.

## Analogía

Con Streams + Tasks:

> Tú defines y programas los pasos.

Con Dynamic Tables:

> Defines el resultado y la frescura que quieres; Snowflake mantiene el resultado.

## Dynamic Tables vs Streams + Tasks

| Streams + Tasks | Dynamic Tables |
|---|---|
| Imperativo | Declarativo |
| Tú defines pasos | Defines el resultado |
| Tú controlas la ejecución | Snowflake mantiene el resultado |
| Muy útil para CDC | Muy útil para pipelines declarativos |

## Regla de examen

**Pipeline de transformación con JOINs que debe mantenerse actualizado automáticamente → Dynamic Table.**
