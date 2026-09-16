# Pruning

## Definition

**Pruning** es el proceso mediante el cual Snowflake evita leer micro-particiones que no pueden contener los datos solicitados.

## How It Works

Snowflake utiliza metadatos de las micro-particiones, como valores mínimos y máximos, para determinar cuáles pueden contener resultados.

Las micro-particiones que no pueden contener resultados se excluyen de la lectura.

## Example

```sql
SELECT *
FROM sales
WHERE sale_date = '2026-01-15';
```

Si los metadatos permiten descartar determinadas micro-particiones, Snowflake no necesita leerlas.

## Exam Clue

Si el caso menciona:

- tabla grande,
- filtro selectivo,
- menos micro-particiones escaneadas,

piensa en **pruning**.

## Related

- Micro-partitions
- Clustering keys
- Search Optimization Service

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
