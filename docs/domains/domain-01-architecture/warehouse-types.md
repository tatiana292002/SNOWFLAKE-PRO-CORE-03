# Warehouse Types

La guía 2026 distingue tres tipos principales.

## Standard Gen 1

Es el warehouse estándar clásico.

## Standard Gen 2

Es la versión más reciente del motor estándar, con mejoras de rendimiento para cargas SQL típicas.

Para el examen, la guía indica pensarlo como el Standard más nuevo/rápido, manteniendo la lógica de tamaños y Scale Up/Scale Out.

## Snowpark-optimized

Es un tipo especial para cargas que necesitan mucha memoria.

La guía indica:

- **16x memoria por nodo** frente a Standard;
- **10x cache local por nodo** frente a Standard.

Casos:

- entrenamiento de ML;
- UDFs pesadas;
- cargas Snowpark con errores de `out of memory`.

## Exam Rule

```text
ML / Snowpark + falta de memoria
→ Snowpark-optimized warehouse
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
