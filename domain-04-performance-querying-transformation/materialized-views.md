# Materialized Views

## ¿Qué es?

Una Materialized View mantiene un resultado precalculado para evitar repetir determinadas operaciones costosas.

## Cuándo pensar en ella

- La misma consulta/agregación costosa se ejecuta repetidamente.
- Los datos son relativamente estables.
- Se quiere reducir el trabajo repetido.

## Analogía

**Materialized View = tener preparada la comida antes de que llegue el cliente.**

## Trampa de examen

No confundas Materialized View con Dynamic Table.

- Materialized View → resultado precalculado para consultas repetitivas.
- Dynamic Table → transformación declarativa que se mantiene actualizada.
- Si el escenario destaca un pipeline con JOINs que necesita mantenerse fresco, piensa en Dynamic Table.
