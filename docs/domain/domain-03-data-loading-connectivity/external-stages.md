# External Stages (stages externos)

> **Dominio 3** · Carga por archivos

Un **named stage** que **apunta a tu propio almacenamiento en la nube**: un bucket de **S3, Azure Blob o GCS**. Los datos siguen viviendo en tu nube; Snowflake solo los lee.

## Cómo se define
- Necesita la **URL** del bucket y **credenciales** de acceso.
- **Buena práctica (y lo que espera el examen):** usar una **[storage integration](./storage-integrations.md)** para no poner llaves de acceso en el código del stage.
- Puede tener **file format** y **directory table** asociados.

> **💡 PIÉNSALO ASÍ:** Es un **acceso directo** a una carpeta de tu nube. No copias nada a Snowflake al crearlo; solo le dices "los archivos están aquí".

## Diferencia con los internos
- A un stage externo **no** haces `PUT`/`GET`: los archivos los deposita tu proveedor de nube (o tu pipeline). Snowflake los **lee** con `COPY INTO` o Snowpipe.
- El **cifrado** y la gestión del bucket los controlas tú, no Snowflake.

> **⚠️ TRAMPA DE EXAMEN:** Si el escenario menciona "sin exponer/incrustar credenciales", la respuesta es **storage integration**, no meter la llave en el stage. No confundas storage integrati[...]

> **✅ REGLA RÁPIDA:** Stage externo = puntero a S3/Azure/GCS + storage integration para las credenciales.

## Ver también
- [storage-integrations.md](./storage-integrations.md) · [stages.md](./stages.md) · [snowpipe.md](./snowpipe.md)
