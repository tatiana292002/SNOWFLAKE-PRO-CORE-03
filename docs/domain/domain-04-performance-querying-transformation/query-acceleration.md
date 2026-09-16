# Query Acceleration Service

## ¿Qué es?

Query Acceleration Service (QAS) proporciona capacidad de cómputo adicional para ayudar con determinadas consultas, especialmente ante picos de trabajo.

## Piensa

> **Picos impredecibles de escaneos grandes.**

## Comparación

| Situación | Solución |
|---|---|
| Una consulta permanentemente pesada | Warehouse más grande |
| Muchas consultas simultáneas | Multi-cluster |
| Pico impredecible de una consulta/escaneo | QAS |

## Trampa

QAS no sustituye el diagnóstico del Query Profile ni corrige una lógica incorrecta de JOIN.
