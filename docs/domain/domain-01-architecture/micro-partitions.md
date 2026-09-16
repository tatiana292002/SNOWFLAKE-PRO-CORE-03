# Micro-partitions

## Definition

Snowflake divide automáticamente los datos de las tablas en **micro-particiones**.

Cada micro-partición contiene un subconjunto de los datos y utiliza almacenamiento columnar.

## Size

La guía indica aproximadamente **50–500 MB** por micro-partición.

## Metadata

Las micro-particiones tienen metadatos, incluyendo valores:

- mínimos (`min`)
- máximos (`max`)

## Why They Matter

Los metadatos permiten a Snowflake determinar qué micro-particiones pueden contener los datos solicitados.

Esto permite **pruning** y reduce la cantidad de datos que debe leer una consulta.

## Exam Focus

Recuerda:

```text
Micro-partition
→ ~50–500 MB
→ columnar
→ min/max metadata
→ permite pruning
```

## Related

- Pruning
- Clustering keys
- Search Optimization Service

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
