# Database Objects

## Hierarchy

La jerarquía indicada por la guía es:

```text
Organization
└── Account
    └── Database
        └── Schema
            └── Objects
```

## Organization / Account Objects

La guía identifica como objetos que viven fuera de una base de datos:

- Virtual Warehouses
- Roles
- Users
- Resource Monitors
- Shares

## Database Objects

Dentro de la jerarquía de base de datos/esquema aparecen:

- Stages
- Tables
- Views
- UDFs
- File Formats
- Stored Procedures
- Pipes
- Sequences
- ML Models
- Applications

## Sequence

Una **Sequence** está diseñada para generar números únicos.

Caso de examen de la guía:

```text
Llave subrogada / números únicos
→ Sequence
```

## Exam Focus

No confundas:

- Warehouse → objeto de cuenta / Compute.
- Table/View/Stage → objetos dentro de la jerarquía de base de datos.
- Sequence → generador de números únicos.

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
