# Table Types

## Permanent

Es el tipo utilizado para datos importantes de producción.

La guía indica:

- Time Travel: hasta 90 días en Enterprise;
- Fail-safe: 7 días.

## Transient

Pensada para datos intermedios o de ETL.

La guía indica:

- Time Travel: 0–1 día;
- sin Fail-safe.

## Temporary

Pensada para datos que solo viven durante la sesión.

La guía indica:

- disponible solo durante la sesión;
- sin Fail-safe.

## External Table

Permite consultar archivos en su ubicación, por ejemplo en un data lake, sin cargarlos como datos internos.

La guía la caracteriza como:

- de solo lectura;
- más lenta;
- con particiones para pruning.

Puede acelerarse colocando una materialized view encima.

## Iceberg Table

Apache Iceberg es un formato abierto.

La guía destaca:

- datos en almacenamiento propio de nube;
- interoperabilidad con motores como Spark y Trino;
- menor dependencia de un formato propietario.

La guía menciona catálogos gestionados por Snowflake y catálogos externos.

## Dynamic Table

Una Dynamic Table representa una transformación declarativa que se mantiene actualizada según la frescura solicitada.

La guía indica que se define mediante:

- Query
- `TARGET_LAG`
- Warehouse

Es especialmente relevante para pipelines de transformación que incluyen joins y deben mantenerse frescos automáticamente.

## Exam Focus

```text
Producción importante → Permanent
ETL/intermedio → Transient
Solo sesión → Temporary
Archivos externos sin cargarlos → External Table
Formato abierto / Spark / Trino → Iceberg
Pipeline declarativo que se refresca solo → Dynamic Table
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
