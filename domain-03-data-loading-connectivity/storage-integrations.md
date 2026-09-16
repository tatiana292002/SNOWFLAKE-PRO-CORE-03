# Storage Integrations

> **Dominio 3** · Conectividad

Objeto que **guarda de forma segura las credenciales** hacia tu almacenamiento en la nube (el rol de IAM en AWS, la identidad en Azure/GCP), para que tus **stages externos** no lleven llaves de acceso escritas en el código.

> **💡 PIÉNSALO ASÍ:** Es una **caja fuerte de credenciales**. El stage externo dice "usa la caja fuerte", y nunca escribes la llave en tu SQL.

## Puntos clave
- Se **reutiliza** en varios stages externos (una integración → muchos stages).
- La crea **ACCOUNTADMIN** (o un rol con `CREATE INTEGRATION`).
- Separa la **configuración de seguridad** (quién administra el acceso a la nube) del **uso diario** (quién crea stages y carga).

> **⚠️ TRAMPA DE EXAMEN:** Hay **tres** objetos que se llaman "integration" y el examen los mezcla:
> - **Storage integration** → credenciales hacia un **bucket** de nube.
> - **API integration** → llamar **servicios/APIs externas** (external functions). Ver [api-integrations.md](./api-integrations.md).
> - **Git integration** → traer/versionar **código desde un repositorio**. Ver [git-integrations.md](./git-integrations.md).

> **✅ REGLA RÁPIDA:** Storage integration = credenciales seguras hacia S3/Azure/GCS, reutilizable, creada por ACCOUNTADMIN.

## Ver también
- [external-stages.md](./external-stages.md) · [api-integrations.md](./api-integrations.md) · [git-integrations.md](./git-integrations.md)
