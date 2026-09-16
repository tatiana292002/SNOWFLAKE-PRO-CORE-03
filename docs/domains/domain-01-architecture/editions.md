# Snowflake Editions

## Standard

La guía la presenta como la plataforma base.

Incluye, entre otros:

- Secure Data Sharing;
- Time Travel de hasta 1 día;
- Fail-safe;
- cifrado;
- SSO/federado;
- MFA.

## Enterprise

Añade capacidades como:

- Multi-cluster warehouses;
- Time Travel hasta 90 días;
- Materialized Views;
- Search Optimization;
- Dynamic Data Masking;
- Row Access Policies;
- Data Metric Functions (DMF);
- Tags;
- clasificación;
- replicación de bases.

## Business Critical

Añade capacidades orientadas a requisitos de seguridad, cumplimiento y continuidad, entre ellas:

- Tri-Secret Secure;
- PrivateLink;
- HIPAA/PCI;
- Failover/Failback.

## VPS

**Virtual Private Snowflake (VPS)** representa un entorno dedicado y aislado.

## Exam Rule

La guía propone resolver preguntas de edición buscando la edición más baja que incluya **todas** las features solicitadas.

Memoria rápida:

```text
Multi-cluster / MV / SOS / masking / DMF / replication
→ Enterprise

Tri-Secret / PrivateLink / failover / HIPAA
→ Business Critical
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
