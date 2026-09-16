# Tasks

## ¿Qué es?

Una Task permite ejecutar SQL o procedimientos de manera programada y puede formar parte de un pipeline.

## Piensa

> **Task = alarma/reloj que ejecuta algo.**

Puede utilizarse:

- En un horario.
- Después de otra Task.
- Encadenando procesos.

## Stream + Task

Patrón clásico:

```text
Stream
  ↓
Detecta cambios
  ↓
Task
  ↓
Procesa cambios
```

## Diferencia

- Stream → registra/detecta cambios.
- Task → ejecuta un proceso.
