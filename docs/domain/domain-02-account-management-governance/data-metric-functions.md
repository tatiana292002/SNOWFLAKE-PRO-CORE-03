# Data Metric Functions (DMF)

## Definition

Las **Data Metric Functions (DMF)** permiten vigilar la calidad de los datos de forma automática y programada.

## Metrics

La guía menciona métricas como:

- `NULL_COUNT`
- `DUPLICATE_COUNT`
- `ROW_COUNT`
- `FRESHNESS`

También permite crear métricas propias.

## Objects

Según la guía, se pueden asignar a:

- tablas;
- dynamic tables;
- external tables;
- Iceberg tables;
- views.

Se configuran con un horario (`schedule`).

## Edition

La guía indica que requieren **Enterprise**.

## Exam Focus

```text
Nulos / duplicados / cantidad de filas / frescura
→ Data Metric Functions
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
