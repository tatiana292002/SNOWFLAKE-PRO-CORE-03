# Search Optimization Service

## ¿Qué es?

Search Optimization Service (SOS) está pensado para acelerar búsquedas selectivas y puntuales en tablas grandes.

## Piensa

> "Necesito encontrar pocas filas dentro de una tabla enorme usando un valor específico."

Ejemplo:

```sql
SELECT *
FROM customers
WHERE customer_id = 123456;
```

## Palabra clave

**Búsqueda puntual + tabla enorme.**

## No confundir

| Escenario | Feature |
|---|---|
| Búsqueda puntual/selectiva | Search Optimization |
| Filtros frecuentes sobre una columna | Clustering |
| Agregación repetitiva | Materialized View |
| Pico de escaneo grande | QAS |
