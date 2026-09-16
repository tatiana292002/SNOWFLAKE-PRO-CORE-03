# Parameters

## Definition

Snowflake tiene parámetros que controlan distintos comportamientos, como formatos, warehouse por defecto o timeouts de consultas.

## Hierarchy

La guía presenta la jerarquía:

```text
Account → User → Session → Object
```

La aplicabilidad exacta depende del parámetro.

## Precedence

Cuando el mismo parámetro está definido en varios niveles, gana el nivel **más específico**.

Ejemplo:

```text
Account: valor A
Session: valor B

→ gana Session
```

## Exam Focus

Pregunta típica:

> Un parámetro está definido a nivel de cuenta y otro valor para la sesión actual. ¿Cuál prevalece?

Respuesta según la guía:

**El parámetro de sesión**, porque es más específico.

## Quick Rule

```text
Más específico > más general
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
