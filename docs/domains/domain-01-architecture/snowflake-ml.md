# Snowflake ML

## Definition

Snowflake ML representa las capacidades para trabajar con el ciclo de vida de Machine Learning dentro de Snowflake.

## Lifecycle

La guía incluye:

1. Preparar datos.
2. Entrenar modelos.
3. Utilizar Snowpark ML para entrenamiento.
4. Registrar modelos como objetos `ML Model`.
5. Ejecutar predicciones sin sacar los datos de la plataforma.

## Snowpark ML

Snowpark ML forma parte del flujo de ML dentro de Snowflake.

Si el entrenamiento necesita mucha memoria, la guía relaciona este caso con un **Snowpark-optimized warehouse**.

## Exam Rule

```text
Entrenar / desplegar un modelo propio
+
mantener los datos dentro de Snowflake
→ Snowflake ML
```

Si aparece además:

```text
Out of memory en ML/Snowpark
→ Snowpark-optimized warehouse
```

## Related

- Snowpark
- Snowpark-optimized warehouses
- Cortex
- ML Models

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
