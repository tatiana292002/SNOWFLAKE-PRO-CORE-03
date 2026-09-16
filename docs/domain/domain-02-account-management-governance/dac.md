# DAC — Discretionary Access Control

## Definition

**DAC** significa Discretionary Access Control.

La guía indica que Snowflake combina RBAC con DAC.

## RBAC vs DAC

| Modelo | Pregunta |
|---|---|
| RBAC | ¿Qué puede hacer cada rol? |
| DAC | ¿Quién controla un objeto individual? |

## Object Owner

Cada objeto tiene un propietario (`owner`).

Ese propietario controla los permisos del objeto y puede gestionar el acceso de acuerdo con las reglas de Snowflake.

## Exam Focus

Si la pregunta enfatiza:

> cada objeto tiene un dueño que controla el acceso

piensa en **DAC**.

## Related

- RBAC
- Ownership
- Managed access
