# Domain 04 — Performance, Querying & Transformation

> SnowPro Core COF-C03 — Dominio 4
>
> Peso en el examen: **21%**

## Objetivo

Diagnosticar problemas de rendimiento, seleccionar la estrategia de optimización adecuada y comprender las principales herramientas de querying y transformación de Snowflake.

## Contenido

- [query-profile.md](query-profile.md)
- [spilling.md](spilling.md)
- [pruning.md](pruning.md)
- [exploding-joins.md](exploding-joins.md)
- [clustering.md](clustering.md)
- [search-optimization.md](search-optimization.md)
- [materialized-views.md](materialized-views.md)
- [query-acceleration.md](query-acceleration.md)
- [workload-management.md](workload-management.md)
- [query-attribution.md](query-attribution.md)
- [account-usage-performance.md](account-usage-performance.md)
- [streams.md](streams.md)
- [tasks.md](tasks.md)
- [dynamic-tables.md](dynamic-tables.md)
- [scd.md](scd.md)
- [udf.md](udf.md)
- [udtf.md](udtf.md)
- [stored-procedures.md](stored-procedures.md)
- [semi-structured-data.md](semi-structured-data.md)
- [unstructured-data.md](unstructured-data.md)
- [window-functions.md](window-functions.md)
- [sql-optimization.md](sql-optimization.md)

## Master Cheat Sheet

| Síntoma | Piensa en |
|---|---|
| Una consulta individual es muy pesada | Warehouse más grande / Scale Up |
| Spilling | Warehouse más grande |
| Muchas consultas simultáneas / queueing | Multi-cluster / Scale Out |
| JOIN genera muchas más filas | Corregir lógica del JOIN |
| Búsqueda puntual en tabla enorme | Search Optimization Service |
| Filtros frecuentes sobre una columna | Clustering |
| Misma agregación costosa repetidamente | Materialized View |
| Picos impredecibles de escaneo | Query Acceleration Service |
| ETL compite con BI | Separar warehouses |
| Detectar cambios | Stream |
| Ejecutar procesos programados | Task |
| Pipeline declarativo con JOINs | Dynamic Table |
| Mantener historia de dimensión | SCD Type 2 |
| JSON / Avro / Parquet / XML | VARIANT / semi-structured |
| Arrays/objetos a filas | FLATTEN |
| Numerar filas | ROW_NUMBER |
| Ranking | RANK |
| Valor anterior | LAG |
| Valor siguiente | LEAD |

## Estrategia de examen

Piensa siempre:

**Problema → síntoma → causa → feature correcta**

No memorices únicamente nombres de funcionalidades. Aprende a distinguir qué problema resuelve cada una.
