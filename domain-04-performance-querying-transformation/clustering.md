# Clustering

## ¿Qué es?

Una clustering key ayuda a organizar físicamente los datos de una tabla para favorecer el pruning.

Es especialmente relevante en tablas grandes donde determinadas columnas aparecen frecuentemente en filtros.

## Analogía

**Clustering = ordenar una biblioteca por temas para encontrar los libros más rápido.**

## Cardinalidad

| Cardinalidad | Idea |
|---|---|
| Muy baja | Poco poder de pruning |
| Muy alta | Puede tener mantenimiento costoso |
| Intermedia | Generalmente más útil |

Ejemplos de cardinalidad muy baja:

- BOOLEAN.
- Columna con muy pocos valores.

Ejemplos de cardinalidad muy alta:

- ID único.
- Timestamp con precisión muy alta.

## Regla de examen

Si el escenario dice que una tabla enorme se filtra frecuentemente por una determinada columna, piensa en **Clustering**.
