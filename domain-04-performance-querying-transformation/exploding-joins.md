# Exploding Joins

## ¿Qué es?

Un exploding join ocurre cuando un JOIN genera muchas más filas de las esperadas.

## Ejemplo conceptual

```text
Tabla A: 100 filas
       +
Tabla B: 100 filas
       ↓
JOIN
       ↓
Resultado inesperado: 100.000 filas
```

Puede indicar:

- Condición de JOIN incompleta.
- Relación muchos-a-muchos no controlada.
- Valores repetidos en ambos lados.

## Solución

**Revisar y corregir la lógica del JOIN.**

## Trampa de examen

No asumas:

```text
JOIN lento → warehouse más grande
```

Si Query Profile muestra un salto enorme de filas en el JOIN, piensa primero en la lógica de la consulta.
