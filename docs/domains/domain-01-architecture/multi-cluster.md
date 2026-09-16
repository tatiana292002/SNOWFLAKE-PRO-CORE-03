# Multi-cluster Warehouses

## Definition

Un **multi-cluster warehouse** puede ejecutar varias copias de un warehouse para repartir la carga entre múltiples usuarios y consultas.

La guía lo presenta como una solución de **Scale Out** y lo sitúa en Enterprise o superior.

## Cluster Counts

Se definen:

- `MIN_CLUSTER_COUNT`
- `MAX_CLUSTER_COUNT`

## Maximized

```text
MIN = MAX
```

Los clusters configurados permanecen activos.

Caso típico: concurrencia alta y constante.

## Auto-scale

```text
MIN < MAX
```

Snowflake puede arrancar o apagar clusters según la demanda.

## Scaling Policies

### Standard

Prioriza reducir la cola.

Arranca otro cluster cuando detecta encolamiento.

### Economy

Prioriza ahorrar créditos.

Espera a que exista suficiente carga para justificar otro cluster y tolera algo de cola.

## Exam Clues

```text
Muchos usuarios / muchas consultas / queuing
→ Multi-cluster

Costo como prioridad + algo de cola aceptable
→ Economy

Reducir cola como prioridad
→ Standard
```

## Related

- Scale Up
- Scale Out
- Warehouse sizing
- Auto-suspend

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
