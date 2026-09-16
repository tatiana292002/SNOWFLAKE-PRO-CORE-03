# Slowly Changing Dimensions (SCD)

## ¿Qué es SCD?

Slowly Changing Dimensions describe estrategias para manejar cambios históricos en tablas de dimensiones.

## Tipo 1

Sobrescribe el valor anterior.

```text
Bogotá → Medellín
```

Solo queda Medellín.

**No conserva historia.**

## Tipo 2

Conserva la historia creando una nueva fila por cada cambio.

Ejemplo:

| Customer | City | Start | End | Current |
|---|---|---|---|---|
| 1 | Bogotá | 2025-01-01 | 2026-02-01 | FALSE |
| 1 | Medellín | 2026-02-01 | NULL | TRUE |

Normalmente se utilizan fechas y una marca de fila vigente.

## Tipo 3

Conserva el valor anterior en una columna adicional.

## Chuleta

```text
Tipo 1 → sobrescribe
Tipo 2 → nueva fila + historia
Tipo 3 → columna con valor anterior
```

## Snowflake

La guía señala `MERGE` como mecanismo habitual para implementar SCD Tipo 2, frecuentemente junto con Streams + Tasks o Dynamic Tables.
