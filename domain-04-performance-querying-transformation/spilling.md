# Spilling

## ¿Qué es?

Spilling ocurre cuando una consulta necesita más memoria de la disponible y parte del procesamiento utiliza almacenamiento.

## Señal importante

En Query Profile puedes encontrar indicadores como:

```text
Bytes spilled to storage
```

## ¿Qué significa?

```text
Consulta necesita más memoria
        ↓
Memoria insuficiente
        ↓
Spilling
        ↓
Considerar Scale Up
        ↓
Warehouse más grande
```

## Trampa de examen

No confundas spilling con concurrencia.

- **Una consulta pesada / falta de memoria → Scale Up.**
- **Muchas consultas simultáneas / cola → Scale Out / Multi-cluster.**
