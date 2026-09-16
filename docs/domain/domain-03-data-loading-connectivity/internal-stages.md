# Internal Stages (stages internos)

> **Dominio 3** · Carga por archivos

Stages cuyo almacenamiento lo **gestiona Snowflake** (cifrado automático incluido). Hay **tres** tipos, y el examen pregunta cuál usar.

## Los tres tipos
| Tipo | Referencia | Cuándo se usa | Detalle clave |
|---|---|---|---|
| **User stage** | `@~` | Archivos **de un solo usuario** | No se altera ni se otorga a otros; uno por usuario |
| **Table stage** | `@%mi_tabla` | Archivos **de una sola tabla** | **No** admite file format propio ni privilegios granulables |
| **Named internal stage** | `@mi_stage` | Uso **flexible y compartido** | Se **otorgan privilegios**, admite file format y directory table |

> **💡 PIÉNSALO ASÍ:** El **user stage** es tu cajón personal; el **table stage** es el cajón pegado a un mueble (esa tabla); el **named stage** es una bodega compartida a la que puedes dar [...])

## Cargar y descargar
- Subes con **`PUT`** y bajas con **`GET`** (desde SnowSQL o Snowflake CLI).
- Snowflake **cifra** los archivos en reposo automáticamente.

> **⚠️ TRAMPA DE EXAMEN:** Solo el **named stage** es un objeto "de verdad" al que puedes **otorgar privilegios** y asociar un **file format**. Los stages de usuario y de tabla **no** se granu[...])

> **✅ REGLA RÁPIDA:** `@~` = usuario · `@%tabla` = tabla · `@nombre` = named (el único gestionable/otorgable).

## Ver también
- [stages.md](./stages.md) · [external-stages.md](./external-stages.md) · [copy-into.md](./copy-into.md)
