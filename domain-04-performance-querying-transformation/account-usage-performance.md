# ACCOUNT_USAGE para Performance

## QUERY_HISTORY

`SNOWFLAKE.ACCOUNT_USAGE.QUERY_HISTORY` proporciona información histórica de consultas.

Puede incluir información como:

- Duración.
- Warehouse utilizado.
- Bytes procesados/escaneados.
- Consultas ejecutadas.

## Query Profile vs ACCOUNT_USAGE

| Herramienta | Uso |
|---|---|
| Query Profile | Diagnóstico de una consulta puntual |
| ACCOUNT_USAGE | Análisis histórico a nivel de cuenta |

## Regla

```text
Una consulta específica → Query Profile
Histórico / múltiples consultas → ACCOUNT_USAGE
```

## Nota

La guía diferencia ACCOUNT_USAGE de INFORMATION_SCHEMA: ACCOUNT_USAGE está orientado a información histórica de cuenta, mientras INFORMATION_SCHEMA sirve para consultar el estado actual de objetos/metadatos.
