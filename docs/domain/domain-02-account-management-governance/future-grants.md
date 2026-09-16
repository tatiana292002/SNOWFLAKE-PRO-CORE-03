# Future Grants

## Definition

Los **future grants** permiten definir permisos que se aplicarán automáticamente a objetos que se creen posteriormente.

## Example

Conceptualmente:

```text
Future tables in schema
→ automatically receive SELECT for a role
```

## Who Can Manage Them

La guía indica que los future grants los puede gestionar:

- `SECURITYADMIN` mediante `MANAGE GRANTS`;
- el owner del schema.

## Exam Focus

Pregunta típica:

> ¿Cómo dar SELECT automáticamente a las tablas que se creen en el futuro?

Respuesta conceptual:

**Future grants**.

## Related

- Managed access
- SECURITYADMIN
- MANAGE GRANTS
- Roles
