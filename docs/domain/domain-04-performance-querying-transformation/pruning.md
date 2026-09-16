# Pruning

## ¿Qué es?

Snowflake almacena datos en micro-particiones y mantiene metadatos que permiten descartar micro-particiones que no pueden contener los valores buscados.

Esto se llama **pruning**.

## Idea

```text
Tabla enorme
   ↓
Muchas micro-particiones
   ↓
Filtro
   ↓
Snowflake descarta particiones irrelevantes
   ↓
Lee menos datos
```

## Señal de problema

Si una consulta escanea casi todas las particiones disponibles, el pruning puede no estar siendo efectivo.

## Relación con otras features

- Búsqueda puntual → Search Optimization.
- Filtros frecuentes sobre una columna → Clustering.
- SQL bien diseñado → también puede mejorar la cantidad de datos procesados.
