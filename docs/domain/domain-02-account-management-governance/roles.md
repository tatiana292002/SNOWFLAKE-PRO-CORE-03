# Roles

## Definition

En Snowflake, los privilegios se asignan a **roles** y los roles se asignan a usuarios o a otros roles.

El objetivo es evitar repartir permisos directamente a cada persona.

## System Roles

La guía identifica:

| Role | Función |
|---|---|
| `ORGADMIN` | Administración a nivel de organización; crea cuentas y habilita replicación |
| `ACCOUNTADMIN` | Rol superior de la cuenta |
| `SECURITYADMIN` | Puede otorgar/revocar permisos mediante `MANAGE GRANTS` |
| `USERADMIN` | Crea y gestiona usuarios y roles |
| `SYSADMIN` | Crea warehouses, bases de datos y objetos |
| `PUBLIC` | Rol que todos tienen por defecto |

## Custom Roles

Los roles personalizados deben formar una jerarquía que finalmente cuelgue de `SYSADMIN`.

## Exam Focus

- Crear usuario o rol → `USERADMIN` o superior.
- Crear warehouse o database → `SYSADMIN` o superior.
- Gestionar grants de forma amplia → `SECURITYADMIN` / `MANAGE GRANTS`.
- Roles personalizados → deben colgar de `SYSADMIN`.

## Source

Basado en la guía fuente.
