# Snowpark

## Definition

Snowpark es un framework para trabajar con DataFrames en:

- Python
- Java
- Scala

## Execution

La guía destaca que la lógica se traduce y ejecuta dentro de Snowflake.

La data no necesita salir de la plataforma para ejecutar la lógica.

El procesamiento aprovecha el compute de los warehouses.

## Use Cases

- Programación de transformaciones complejas.
- Trabajo con DataFrames.
- Desarrollo de lógica en Python, Java o Scala.
- Machine Learning mediante Snowpark ML.

## Mental Model

```text
Snowpark = programar lógica con DataFrames
            sin sacar los datos de Snowflake
```

## Exam Focus

```text
DataFrames + Python/Java/Scala
→ Snowpark
```

Si además el problema es una carga pesada de ML/Snowpark con falta de memoria:

```text
→ Snowpark-optimized warehouse
```

## Related

- Snowpark-optimized warehouse
- Notebooks
- Snowflake ML
- Snowflake CLI

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
