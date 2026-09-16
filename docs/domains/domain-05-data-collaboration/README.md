# Domain 5: Data Collaboration

## Descripción General
Este dominio cubre los mecanismos de compartición segura de datos en Snowflake, replicación entre regiones y proveedores de nube, y colaboración a través del marketplace.

## Temas Clave
- **Compartición Segura de Datos (Secure Data Sharing)**:
  - Concepto de Provider (proveedor) y Consumer (consumidor).
  - Objetos Share (`CREATE SHARE`, `GRANT ... ON SHARE`).
  - Vistas seguras (Secure Views) y funciones definidas por el usuario seguras (Secure UDFs).
  - Reader Accounts (para consumidores sin cuenta propia de Snowflake).
- **Snowflake Marketplace y Data Exchange**:
  - Snowflake Marketplace (conjuntos de datos públicos y de terceros).
  - Private Data Exchange para intercambio de datos corporativo o privado.
- **Replicación y Alta Disponibilidad (Replication & Failover)**:
  - Replicación entre regiones y entre diferentes proveedores de nube (Cross-cloud / Cross-region replication).
  - Cuentas de réplica, Failover Groups y Business Continuity / Disaster Recovery (BCDR).
