# Alerts

## Definition

Una **Alert** ejecuta una consulta de forma periódica y comprueba si se cumple una condición.

## Behavior

Conceptualmente:

```text
Schedule
   ↓
Run query
   ↓
Condition?
   ↓
Action
```

La acción puede incluir el envío de una notificación.

## Example

Una alerta puede detectar una condición como:

```text
más de 100 filas con error
```

y disparar una acción.

## Exam Focus

```text
Comprobar periódicamente una condición
→ Alert

Avisar al usuario/sistema
→ Notification
```

## Related

- Notifications
- Tasks
- Monitoring
