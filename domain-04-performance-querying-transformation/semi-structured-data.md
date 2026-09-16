# Semi-Structured Data

## ¿Qué es?

Snowflake trabaja con datos semiestructurados como:

- JSON
- Avro
- Parquet
- XML

La guía los relaciona con el tipo `VARIANT`.

## VARIANT

Permite almacenar datos semiestructurados y navegar por sus elementos.

Se puede acceder a campos mediante:

```text
.
[]
```

## FLATTEN

`FLATTEN` permite expandir elementos de estructuras anidadas, como arrays u objetos, a filas que pueden procesarse mediante SQL.

## Modelo mental

```text
JSON
  ↓
VARIANT
  ↓
campo / subcampo
  ↓
FLATTEN
  ↓
filas
```

## Trampa

Semi-structured no significa unstructured.

- Semi-structured → JSON, Avro, Parquet, XML.
- Unstructured → documentos, imágenes y otros archivos.
