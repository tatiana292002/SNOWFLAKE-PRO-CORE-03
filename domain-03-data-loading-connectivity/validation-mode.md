# VALIDATION_MODE

> **Dominio 3** · Carga por archivos

Opción de `COPY INTO` que **valida los archivos sin cargar nada**: sirve para **ver los errores antes** de la carga real.

## Valores
| Valor | Qué hace |
|---|---|
| `RETURN_ERRORS` | Devuelve **todos los errores** encontrados en los archivos |
| `RETURN_n_ROWS` | Intenta parsear las **primeras n filas**; falla si alguna tiene error |
| `RETURN_ALL_ERRORS` | Devuelve errores de todos los archivos, incluidos los de cargas parciales previas |

> **💡 PIÉNSALO ASÍ:** Es un **simulacro de carga**: pruebas que los datos entran bien, pero sin dejar nada en la tabla.

## Relacionado
- La función de tabla **`VALIDATE()`** inspecciona los errores de una carga **ya ejecutada**.

> **⚠️ TRAMPA DE EXAMEN:** `VALIDATION_MODE` **no carga datos** y **no se puede usar** junto con transformaciones (un `COPY` con `SELECT`). Es solo para validar.

> **✅ REGLA RÁPIDA:** ¿Ver errores **antes** de cargar? → `VALIDATION_MODE`. ¿Revisar errores **después** de cargar? → `VALIDATE()`.

## Ver también
- [copy-into.md](./copy-into.md) · [file-formats.md](./file-formats.md)
