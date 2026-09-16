# Network Policies

## Definition

Las Network Policies controlan desde qué direcciones IP se permite conectarse a Snowflake.

## Lists

La guía menciona:

- `ALLOWED_IP_LIST`
- `BLOCKED_IP_LIST`

## Precedence

La lista de bloqueadas gana.

Si una IP aparece tanto en allowed como en blocked:

```text
BLOCKED → acceso bloqueado
```

Además, una política aplicada a nivel de usuario tiene prioridad sobre la política de cuenta para ese usuario.

## Exam Focus

```text
Allowed + Blocked
→ Blocked wins

User policy + Account policy
→ User policy has priority for that user
```

## Source

Basado en la guía fuente.
