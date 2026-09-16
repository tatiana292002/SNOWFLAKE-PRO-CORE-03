# Connectors

> **Dominio 3** · Conectividad

Los **connectors** son **integraciones ya construidas con herramientas externas**, para mover datos hacia/desde Snowflake sin programar la conexión desde cero.

## Ejemplos
- **Conector de Kafka** (ingesta desde topics). Ver [kafka.md](./kafka.md).
- **Conector de Spark** (leer/escribir desde Spark).
- Conectores de ingesta hacia/desde otras plataformas del ecosistema.

> **💡 PIÉNSALO ASÍ:** Si el **driver** es el enchufe genérico, el **connector** es un **cable a medida** ya fabricado para una herramienta concreta (Kafka, Spark...).

## Connector vs Driver
- **Connector** → integración lista con una **herramienta** (Kafka, Spark).
- **Driver** → conectar un **lenguaje/app** (JDBC, ODBC, Python...). Ver [drivers.md](./drivers.md).

> **✅ REGLA RÁPIDA:** ¿Integración lista con una herramienta (Kafka/Spark)? → connector. ¿Conectar tu propio código? → driver.

## Ver también
- [drivers.md](./drivers.md) · [kafka.md](./kafka.md)
