# Snowflake Caching

La guía distingue **tres caches**.

## 1. Query Result Cache

También llamado **Result Cache**.

- Vive en **Cloud Services**.
- La guía indica una duración de **24 horas**, renovable al reutilizarlo.
- Tiene alcance global.
- No necesita que un warehouse esté encendido.

### Conditions

La guía indica que el result cache se reutiliza cuando, entre otras condiciones:

- la consulta es idéntica;
- los privilegios son compatibles;
- los datos no cambiaron;
- no se usan funciones volátiles como `CURRENT_TIMESTAMP` o `RANDOM`.

## 2. Metadata Cache

También vive en **Cloud Services**.

La guía lo relaciona con metadatos como:

- min/max de micro-particiones;
- conteos.

Puede responder determinados metadatos sin que el warehouse esté encendido.

## 3. Warehouse / Local Disk Cache

Es la cache de datos local del warehouse, ubicada en su almacenamiento local/SSD.

- Existe mientras el warehouse está encendido.
- Se pierde cuando el warehouse se suspende.
- También se pierde al redimensionarlo.

## Comparison

| Cache | Ubicación | Warehouse encendido |
|---|---|---|
| Query Result Cache | Cloud Services | No |
| Metadata Cache | Cloud Services | No |
| Warehouse / Local Disk Cache | SSD del warehouse | Sí |

## Exam Focus

```text
Resultado idéntico → Result Cache
Metadatos → Metadata Cache
Datos locales del warehouse → Warehouse Cache
```

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
