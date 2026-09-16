# Drivers

> **Dominio 3** · Conectividad

Los **drivers** permiten que **aplicaciones y lenguajes de programación hablen directamente con Snowflake**.

## Los principales
- **JDBC** (Java), **ODBC** (genérico), y conectores para **Python**, **Node.js**, **Go**, **.NET**, **PHP**.

> **💡 PIÉNSALO ASÍ:** El driver es el **enchufe/adaptador** que conecta tu app o tu lenguaje al "toma corriente" de Snowflake.

## Driver vs Connector vs Integration (no confundir)
- **Driver** → conecta un **lenguaje/app** a Snowflake (JDBC, ODBC, Python...).
- **Connector** → integración **ya construida con una herramienta** externa (Kafka, Spark). Ver [connectors.md](./connectors.md).
- **Integration** → un **objeto** en Snowflake (storage / API / Git).

## Detalle útil
- Para conexiones programáticas se usa mucho la **autenticación por par de llaves (key-pair)** en vez de contraseña.

> **✅ REGLA RÁPIDA:** Driver = conectar un lenguaje/app (JDBC, ODBC, Python, Go, .NET, Node.js).

## Ver también
- [connectors.md](./connectors.md) · [snowflake-cli.md](./snowflake-cli.md)
