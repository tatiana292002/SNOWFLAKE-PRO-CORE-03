# Managed Access Schemas

## Definition

Un schema de acceso gestionado (**managed access**) centraliza la administración de grants.

## Behavior

En un schema normal, el owner de un objeto puede repartir permisos.

En un schema managed access:

- el owner del objeto no puede repartir permisos;
- el owner del schema puede hacerlo;
- también puede hacerlo alguien con `MANAGE GRANTS`.

## Exam Trap

Si un usuario es owner de una tabla pero no puede conceder un privilegio sobre ella, comprueba si la tabla está en un **managed access schema**.

## Quick Rule

```text
Normal schema → object owner can grant
Managed access → schema owner / MANAGE GRANTS controls grants
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
