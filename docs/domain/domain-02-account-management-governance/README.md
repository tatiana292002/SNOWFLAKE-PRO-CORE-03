# Domain 2: Account Management and Governance

## Descripción General
Este dominio abarca la administración de cuentas, gestión de usuarios, roles, seguridad, costos y gobierno del dato en Snowflake.

## Temas Clave
- **Control de Acceso Basado en Roles (RBAC)**:
  - Jerarquía de roles del sistema (`ACCOUNTADMIN`, `SECURITYADMIN`, `USERADMIN`, `SYSADMIN`, `PUBLIC`).
  - Asignación de privilegios y creación de roles personalizados.
- **Seguridad y Redes**:
  - Políticas de red (Network Policies / IP Whitelisting).
  - Autenticación multifactor (MFA), SSO y Federated Authentication (SAML 2.0).
- **Gobierno del Dato (Data Governance)**:
  - Enmascaramiento dinámico de datos (Dynamic Data Masking).
  - Políticas de acceso a nivel de fila (Row Access Policies).
  - Etiquetas de objetos (Object Tagging) y seguimiento de linaje de datos.
- **Gestión de Cuentas y Costos**:
  - Esquema `ACCOUNT_USAGE` vs `INFORMATION_SCHEMA`.
  - Resource Monitors y control de consumo de créditos.
