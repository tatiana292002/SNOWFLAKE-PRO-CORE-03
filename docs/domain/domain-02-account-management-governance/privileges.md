# Privileges

## Definition

Un privilegio determina qué puede hacer un rol sobre un objeto.

Los privilegios se conceden a roles, no directamente a las personas.

## Permission Chain

Para consultar una tabla, la guía destaca esta cadena:

```text
USAGE(database)
+
USAGE(schema)
+
SELECT(table)
+
USAGE(warehouse)
```

Tener solamente `SELECT` sobre la tabla no garantiza que el usuario pueda consultarla.

## Common Examples

- `USAGE` en database.
- `USAGE` en schema.
- `SELECT` en table.
- `USAGE` en warehouse.
- `EXECUTE` para ejecutar procedimientos/funciones según el caso.

## Exam Trap

> El usuario tiene `SELECT` pero no puede consultar.

Revisa primero:

1. `USAGE` en la database.
2. `USAGE` en el schema.
3. `USAGE` en el warehouse.
4. Si el schema usa managed access.

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
