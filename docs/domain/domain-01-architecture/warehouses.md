# Virtual Warehouses

## Definition

Un **Virtual Warehouse** es el motor de cómputo que ejecuta consultas y cargas de datos.

No almacena permanentemente los datos; los lee desde Storage, los procesa y devuelve resultados.

## Scale Up

**Scale Up** significa aumentar el tamaño del warehouse.

Úsalo como concepto de examen cuando el problema es:

- una consulta individual compleja,
- una consulta lenta,
- falta de memoria,
- `spilling`.

## Scale Out

**Scale Out** significa aumentar el número de clusters mediante un **multi-cluster warehouse**.

Úsalo cuando el problema es:

- muchos usuarios,
- muchas consultas simultáneas,
- concurrencia,
- consultas en cola.

## Quick Rule

```text
Una consulta pesada / falta de memoria → Scale Up
Muchas consultas / concurrencia / cola → Scale Out
```

## Workload Management

La guía recomienda separar cargas de trabajo diferentes en warehouses dedicados, por ejemplo:

- ETL/ELT
- BI
- consultas ad-hoc

Esto evita que cargas muy diferentes compitan por el mismo recurso.

## Auto-suspend / Auto-resume

- **Auto-suspend** apaga el warehouse después de un periodo sin uso.
- **Auto-resume** permite que vuelva a iniciarse cuando llega una consulta.
- La guía indica un valor por defecto de auto-suspend de **600 segundos (10 minutos)**.

## Exam Focus

No intentes resolver un problema de concurrencia simplemente aumentando el tamaño de un warehouse: primero identifica si el problema es Scale Up o Scale Out.

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
