# Domain 1: Snowflake Architecture

## Descripción General
Este dominio cubre los fundamentos de la arquitectura multicloud híbrida de Snowflake, separando almacenamiento, cómputo y servicios en la nube.

## Temas Clave
- **Capa de Almacenamiento (Database Storage)**:
  - Micro-particiones y almacenamiento columnar.
  - Inmutabilidad de los datos y compresión automática.
- **Capa de Cómputo (Query Processing / Virtual Warehouses)**:
  - Warehouses virtuales: escalado vertical (scale up) y horizontal (scale out / multi-cluster).
  - Políticas de escalado (Standard vs Economy).
- **Capa de Servicios en la Nube (Cloud Services Layer)**:
  - Autenticación, gestión de infraestructura, optimización de consultas y gestión de metadatos.
- **Mecanismos de Caché en Snowflake**:
  - Metadata Cache (Cloud Services).
  - Local Disk Cache / SSD Cache (Virtual Warehouses).
  - Result Cache (Persisted Query Results - 24h).
