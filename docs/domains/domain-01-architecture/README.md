# Domain 1 — Snowflake AI Data Cloud Features and Architecture

## Scope

Domain 1 representa el **31%** del examen SnowPro Core COF-C03 según la guía de estudio utilizada como fuente.

Este directorio divide el contenido en archivos pequeños y autónomos para facilitar el estudio humano y la consulta por IA.

## Files

### Architecture and storage
- `architecture.md`
- `micro-partitions.md`
- `pruning.md`

### Warehouses and compute
- `warehouses.md`
- `warehouse-sizing.md`
- `multi-cluster.md`
- `caching.md`
- `warehouse-types.md`

### Interfaces and objects
- `snowflake-interfaces.md`
- `database-objects.md`
- `table-types.md`
- `views.md`
- `parameters.md`

### Editions
- `editions.md`

### Development and AI
- `notebooks.md`
- `streamlit.md`
- `snowpark.md`
- `cortex.md`
- `snowflake-ml.md`

## Exam map

| Situation | Concept |
|---|---|
| Separación de administración, cómputo y almacenamiento | Architecture |
| Bloques físicos y metadatos min/max | Micro-partitions |
| Evitar leer bloques que no pueden contener resultados | Pruning |
| Una consulta pesada / falta de memoria | Scale Up |
| Muchas consultas simultáneas / cola | Multi-cluster |
| Reutilizar resultados | Query Result Cache |
| SQL moderno desde terminal y despliegues | Snowflake CLI |
| Jerarquía de objetos | Database Objects |
| Generar números únicos | Sequence |
| Parámetros en conflicto | Gana el nivel más específico |
| Preguntas en lenguaje natural sobre tablas | Cortex Analyst |
| Búsqueda semántica sobre documentos/texto | Cortex Search |
| ML/Snowpark con falta de memoria | Snowpark-optimized warehouse |

## Source

Contenido basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`, versión indicada en la guía como actualizada al 8 de julio de 2026. La propia guía recomienda contrastar límites exactos y disponibilidad de features recientes con la documentación oficial de Snowflake antes del examen.
