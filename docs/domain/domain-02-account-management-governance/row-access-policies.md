# Row Access Policies

## Definition

Una **Row Access Policy** controla qué **filas** puede ver un usuario según su contexto/rol.

## Key Distinction

```text
Dynamic Data Masking → columnas
Row Access Policy     → filas
```

## Example

Una política puede hacer que un usuario vea únicamente las filas correspondientes a su región o función.

## Exam Focus

Si el problema habla de:

- filtrar filas;
- mostrar subconjuntos de registros según el usuario/rol;

piensa en **Row Access Policy**.

## Related

- Masking
- RBAC
- Tags
