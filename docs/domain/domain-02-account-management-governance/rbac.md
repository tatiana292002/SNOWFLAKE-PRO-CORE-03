# RBAC — Role-Based Access Control

## Definition

**RBAC** significa Role-Based Access Control.

En este modelo:

```text
Privileges → Roles → Users
```

Los privilegios se asignan a roles y los roles se asignan a usuarios.

## Purpose

Permite gestionar permisos por función en lugar de administrar permisos individualmente para cada usuario.

## Example

```text
Role: SALES_ANALYST
    ├── USAGE(database)
    ├── USAGE(schema)
    └── SELECT(table)

User: Ana
    └── SALES_ANALYST
```

## Exam Focus

RBAC responde a:

> ¿Qué puede hacer este rol?

No responde por sí solo a:

> ¿Quién controla este objeto concreto?

Para esto último, la guía introduce DAC/ownership.

## Related

- DAC
- Roles
- Privileges
- Ownership
