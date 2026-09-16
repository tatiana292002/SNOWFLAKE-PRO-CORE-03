# Role Hierarchy

## Definition

Los roles pueden otorgarse a otros roles, formando una jerarquía.

Esto permite heredar los privilegios del rol otorgado.

## Recommended Structure

La guía indica que los roles personalizados deben colgar de `SYSADMIN`, directamente o a través de otros roles personalizados.

```text
SYSADMIN
├── DATA_ENGINEER
│   └── ETL_ANALYST
└── BI_ANALYST
```

El diagrama anterior es solo un ejemplo conceptual de jerarquía.

## System Roles

La guía identifica una jerarquía funcional:

```text
ORGADMIN
└── ACCOUNTADMIN
    └── SECURITYADMIN
        └── USERADMIN

SYSADMIN
└── Custom Roles
```

## Exam Focus

La regla explícita de la guía:

**Los roles personalizados deben colgar de `SYSADMIN`.**

## Source

Basado en la guía fuente.
