# Snowflake Architecture

## Definition

Snowflake separa la plataforma en tres capas principales:

1. **Cloud Services**
2. **Compute**
3. **Storage**

La separación permite que almacenamiento y computación escalen de forma independiente.

## Cloud Services

Gestiona funciones como:

- Autenticación
- Control de acceso
- Metadatos
- Optimización de consultas
- Seguridad

## Compute

El procesamiento de consultas y cargas de datos se realiza mediante **Virtual Warehouses**.

El warehouse proporciona computación; los datos permanentes están en Storage.

## Storage

Los datos se almacenan de forma comprimida y organizada por columnas.

## Mental model

```text
Cloud Services = administración y coordinación
Compute        = procesamiento
Storage        = datos
```

## Exam Focus

- No confundir Storage con Compute.
- Virtual Warehouse pertenece a Compute.
- Cloud Services gestiona autenticación, acceso, metadatos, optimización y seguridad.
- Las capas están separadas.

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`, sección de arquitectura de Domain 1.
