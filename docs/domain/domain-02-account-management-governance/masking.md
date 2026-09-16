# Dynamic Data Masking

## Definition

Dynamic Data Masking protege datos sensibles ocultando valores de **columnas** según el rol.

## Column-Level Security

La idea central es:

```text
Masking → columns
```

No debe confundirse con Row Access Policy, que controla filas.

## Tag-Based Masking

La guía también describe **tag-based masking**:

1. Se etiqueta una columna, por ejemplo `PII`.
2. Se asocia una masking policy al tag.
3. Las columnas con ese tag reciben la protección automáticamente.

## Example

```text
Tag: PII = true
        ↓
Masking policy
        ↓
Columnas etiquetadas como PII
```

## Exam Focus

```text
Ocultar columnas sensibles → Dynamic Data Masking
Aplicar automáticamente por clasificación/tag → Tag-based masking
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
