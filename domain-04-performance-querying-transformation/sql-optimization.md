# SQL Optimization

## Objetivo

Optimizar consultas reduciendo datos procesados y evitando trabajo innecesario.

## 1. Filtrar temprano

Aplica filtros para reducir la cantidad de datos antes de operaciones costosas cuando sea apropiado.

```sql
SELECT ...
FROM large_table
WHERE status = 'ACTIVE';
```

## 2. Evitar SELECT *

En tablas anchas, seleccionar únicamente las columnas necesarias puede reducir datos procesados.

```sql
SELECT customer_id, amount
FROM sales;
```

en lugar de:

```sql
SELECT *
FROM sales;
```

## 3. Agregar antes de unir

Cuando sea correcto para la lógica de negocio:

```text
Datos grandes
    ↓
Agregación
    ↓
Menos filas
    ↓
JOIN
```

Reducir filas antes del JOIN puede disminuir el trabajo posterior.

## 4. Revisar JOINs

Si un JOIN genera muchas más filas de las esperadas, no asumas que necesitas un warehouse mayor.

Primero revisa:

- Condiciones.
- Cardinalidad.
- Relaciones muchos-a-muchos.
- Duplicados.

## Regla final

Una buena optimización empieza por reducir el trabajo que la consulta realmente necesita hacer.
