# ACCOUNT_USAGE

## Definition

`SNOWFLAKE.ACCOUNT_USAGE` contiene información histórica a nivel de cuenta.

## Scope

La guía lo compara con `INFORMATION_SCHEMA`:

| | ACCOUNT_USAGE | INFORMATION_SCHEMA |
|---|---|---|
| Alcance | Toda la cuenta | Una database |
| Latencia | 45 min–3 h de retraso | Tiempo real |
| Historia | Hasta 365 días | Días o pocos meses |
| Objetos borrados | Sí | No |

## Common Views

La guía menciona:

- `QUERY_HISTORY`
- `WAREHOUSE_METERING_HISTORY`
- `LOGIN_HISTORY`

## When to Use

```text
Historia larga / objetos borrados
→ ACCOUNT_USAGE

Estado actual inmediato de una database
→ INFORMATION_SCHEMA
```

## Query Attribution

La guía también menciona vistas de **query attribution** para atribuir consumo de compute a la consulta, usuario o proceso que lo generó.

## Exam Focus

No confundas:

```text
ACCOUNT_USAGE = histórico, nivel cuenta
INFORMATION_SCHEMA = estado actual, nivel database
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
