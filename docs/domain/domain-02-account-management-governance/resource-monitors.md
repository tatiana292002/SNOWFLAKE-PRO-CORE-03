# Resource Monitors

## Definition

Los **Resource Monitors** controlan el consumo de créditos de los warehouses.

## Configuration

Se define una cuota y acciones asociadas a determinados porcentajes de consumo.

Acciones indicadas:

- `NOTIFY`
- `SUSPEND`
- `SUSPEND_IMMEDIATE`

## Actions

### NOTIFY

Envía un aviso.

### SUSPEND

Suspende el warehouse después de permitir terminar lo que está ejecutándose.

### SUSPEND_IMMEDIATE

Suspende de inmediato.

## Exam Trap

Resource Monitor controla **créditos de warehouses**.

No debe confundirse con un mecanismo para controlar directamente el costo del almacenamiento en disco.

## Quick Rule

```text
Warehouse credits → Resource Monitor
Storage cost → no asumir Resource Monitor
```

## Source

Basado en la guía fuente.
