# Secondary Roles

## Definition

Un usuario puede activar varios roles secundarios además de su rol primario durante una sesión.

## Activation

La guía menciona:

```sql
USE SECONDARY ROLES ALL;
```

Esto activa los roles secundarios disponibles para la sesión.

## Effect

Los privilegios de los roles activados se suman para esa sesión.

El rol primario no cambia.

## Exam Question Pattern

> Un usuario necesita sumar temporalmente privilegios de otros roles sin cambiar su rol principal.

Respuesta:

**Secondary roles**.

## Related

- RBAC
- Role hierarchy
- Account roles
