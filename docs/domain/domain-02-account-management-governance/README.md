# Domain 2 — Account Management and Data Governance

## Scope

Domain 2 representa el **20%** del examen SnowPro Core COF-C03 según la guía fuente.

Este directorio separa los conceptos de administración de cuentas, RBAC/DAC, autenticación, gobernanza, seguridad, calidad y control de costos en archivos pequeños y autónomos.

## Files

### Access control
- `roles.md`
- `privileges.md`
- `role-hierarchy.md`
- `rbac.md`
- `dac.md`
- `ownership.md`
- `managed-access.md`
- `future-grants.md`
- `database-roles.md`
- `secondary-roles.md`

### Account and authentication
- `account-identifiers.md`
- `authentication.md`
- `network-policies.md`

### Data governance
- `masking.md`
- `row-access-policies.md`
- `tagging.md`
- `privacy-policies.md`
- `trust-center.md`
- `alerts.md`
- `notifications.md`
- `data-lineage.md`
- `data-metric-functions.md`

### Cost and usage
- `resource-monitors.md`
- `budgets.md`
- `account-usage.md`

## Exam map

| Scenario | Concept |
|---|---|
| Qué puede hacer un rol | RBAC / privileges |
| Quién controla un objeto | DAC / ownership |
| SELECT pero no puede consultar | Revisar USAGE en DB, schema y warehouse |
| Crear usuarios o roles | USERADMIN |
| Conceder permisos ampliamente | SECURITYADMIN / MANAGE GRANTS |
| Crear warehouses/bases | SYSADMIN |
| Roles personalizados | Deben colgar de SYSADMIN |
| Permisos automáticos para objetos futuros | Future grants |
| Varios roles activos en una sesión | Secondary roles |
| Permisos granulares dentro de una DB | Database roles |
| Acceso restringido por IP | Network policies |
| Ocultar columnas sensibles | Dynamic Data Masking |
| Filtrar filas | Row Access Policy |
| Aplicar masking por clasificación/tag | Tag-based masking |
| Clasificar objetos/columnas | Object tagging |
| Revisar postura de seguridad | Trust Center |
| Avisar cuando ocurre una condición | Alert + Notification |
| Saber de dónde vino un dato | Data lineage |
| Vigilar nulos/duplicados/frescura | Data Metric Functions |
| Controlar créditos de warehouses | Resource Monitor |
| Controlar costos de compute + storage + serverless | Budgets |
| Historial de uso de toda la cuenta | ACCOUNT_USAGE |

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`, actualizada según la guía al 8 de julio de 2026. No se añaden aquí detalles que no estén respaldados por la fuente.
