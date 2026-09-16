# Snowflake Notebooks

## Definition

Snowflake Notebooks es un entorno de notebooks, similar al estilo Jupyter, que combina:

- celdas de código;
- SQL;
- texto.

La guía indica que se ejecuta directamente dentro de Snowflake y sobre un warehouse.

## Use Cases

- Explorar datos.
- Prototipar modelos.
- Combinar SQL y Python en un mismo documento.
- Trabajar sin sacar los datos de la plataforma.

## Mental Model

```text
Notebook = laboratorio interactivo dentro de Snowflake
```

## Exam Focus

La idea clave es que el notebook trabaja dentro de Snowflake y usa recursos de compute.

La guía también indica que el warehouse por defecto para Notebooks no se evalúa en detalle hasta que esa capacidad esté disponible de forma general (GA); basta con reconocer su existencia según el material.

## Related

- Snowpark
- Streamlit
- Snowflake ML
- Warehouses

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
