# Workload Management

## ¿Qué es?

Workload Management consiste en organizar las cargas de trabajo para evitar que procesos muy diferentes compitan por los mismos recursos.

## Ejemplo

Separar:

```text
Warehouse BI
├── Dashboards
└── Consultas de analistas

Warehouse ETL
├── Cargas
└── Transformaciones
```

en lugar de hacer que ETL pesado y BI compartan el mismo warehouse.

## Regla

**Cargas diferentes → considerar warehouses separados.**

Esto puede reducir contención, colas y comportamiento impredecible.

## Trampa

No resolver automáticamente un problema de workloads aumentando el tamaño de un único warehouse. Primero identifica si el problema es concurrencia o competencia entre cargas.
