# Views

## Standard View

Una Standard View guarda la definición de la consulta.

La consulta se ejecuta cuando se utiliza la vista.

## Materialized View

Una Materialized View mantiene un resultado precalculado.

La guía la relaciona con casos donde existe una agregación cara y repetida sobre datos relativamente estables.

## Secure View

Una Secure View oculta la definición SQL de la vista a usuarios que no son propietarios.

Es útil cuando se quiere exponer datos sin revelar:

- la lógica SQL;
- las tablas subyacentes.

## Comparison

| Tipo | Idea principal |
|---|---|
| Standard | Guarda la consulta |
| Materialized | Mantiene resultado precalculado |
| Secure | Oculta la definición SQL |

## Exam Focus

```text
Consulta normal → Standard View
Resultado precalculado → Materialized View
Ocultar definición SQL → Secure View
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
