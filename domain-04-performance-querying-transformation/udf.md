# UDF — User-Defined Functions

## ¿Qué es?

Una UDF es una función definida por el usuario.

Permite encapsular lógica reutilizable.

## SQL UDF

La guía señala que una SQL UDF puede consultar tablas/vistas dentro de su lógica según el contexto permitido.

## JavaScript UDF

Una JavaScript UDF no ejecuta SQL para consultar tablas.

## Regla de examen

```text
SQL UDF
→ puede consultar datos según el contexto

JavaScript UDF
→ no ejecuta SQL
```

## No confundir

UDF devuelve un valor/resultado de función; una UDTF devuelve un conjunto de filas.
