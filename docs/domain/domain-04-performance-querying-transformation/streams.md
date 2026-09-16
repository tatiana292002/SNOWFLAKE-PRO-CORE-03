# Streams

## ¿Qué es?

Un Stream registra cambios realizados sobre datos y permite trabajar con procesamiento incremental / CDC.

Piensa:

> **Stream = cámara que observa los cambios.**

## Cambios típicos

- INSERT
- UPDATE
- DELETE

## Objetivo

Procesar los cambios en lugar de reprocesar toda la tabla.

## Patrón clásico

```text
Tabla
  ↓
Cambios
  ↓
Stream
  ↓
Task
  ↓
Procesamiento
```

## Trampa

Stream detecta/registra cambios; no es el mecanismo que por sí mismo programa la ejecución.
