# Ownership

## Definition

La guía indica que quien crea un objeto se convierte en su **owner**.

Solo existe un owner a la vez.

## Owner Capabilities

El owner tiene todos los permisos sobre el objeto y puede repartir permisos sobre él, sujeto a las reglas del esquema y del modelo de acceso.

## Ownership Transfer

La propiedad puede transferirse según los privilegios disponibles.

## Managed Access Exception

En un esquema de **managed access**, los propietarios de los objetos ya no pueden repartir permisos directamente.

El control pasa al owner del schema o a alguien con `MANAGE GRANTS`.

## Exam Focus

```text
Creador del objeto → owner
Managed access → el owner del objeto no administra grants directamente
```

## Source

Basado en la guía fuente.
