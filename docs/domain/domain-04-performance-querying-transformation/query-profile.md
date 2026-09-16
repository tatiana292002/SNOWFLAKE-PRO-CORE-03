# Query Profile

## ¿Qué es?

Query Profile permite inspeccionar cómo se ejecutó una consulta y localizar las operaciones que están causando problemas de rendimiento.

## ¿Qué buscar?

- Operaciones costosas.
- Cantidad de filas.
- Bytes procesados.
- Particiones escaneadas.
- Spilling.
- JOINs que producen cantidades inesperadas de filas.
- Etapas que consumen mucho tiempo.

## Regla de examen

No mires únicamente el tiempo total de la consulta. Busca **qué operación está causando el problema**.

## Patrón

```text
Query lenta
   ↓
Abrir Query Profile
   ↓
Identificar operación problemática
   ↓
Determinar causa
   ↓
Aplicar la optimización correspondiente
```
