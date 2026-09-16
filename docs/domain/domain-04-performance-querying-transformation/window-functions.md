# Window Functions

## ¿Qué son?

Las Window Functions permiten realizar cálculos sobre un conjunto relacionado de filas sin colapsar las filas como ocurre con un `GROUP BY`.

## Funciones que debes reconocer

```sql
ROW_NUMBER()
RANK()
LAG()
LEAD()
```

## Estructura mental

```text
PARTITION BY
    ↓
Grupo lógico
    ↓
ORDER BY
    ↓
Orden dentro del grupo
    ↓
Window Function
```

## Chuleta

| Función | Idea |
|---|---|
| ROW_NUMBER() | Numera filas |
| RANK() | Asigna ranking |
| LAG() | Accede a una fila anterior |
| LEAD() | Accede a una fila siguiente |

## Trampa

Window Function no es lo mismo que `GROUP BY`: las filas originales pueden permanecer en el resultado.
