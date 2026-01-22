# RetailPlus Data Pipeline: ETL

## Descripción del notebook
Este proyecto implementa un pipeline de Ingeniería de Datos para **RetailPlus Perú**, una cadena de supermercados con presencia nacional (fictiocio)

El objetivo principal es procesar datos transaccionales crudos (Raw Data), limpiarlos y estructurarlos en una arquitectura de datos moderna (Medallion Architecture) para habilitar el análisis de negocio sobre reclamos, ventas y comportamiento del cliente.

## Tecnologías y Herramientas
* **Lenguaje:** Python (PySpark) y SQL.
* **Plataforma:** Databricks.
* **Librerías Clave:** `pyspark.sql.functions` (para transformaciones).
* **Conceptos Aplicados:** ETL, Data Quality, Data Modeling.

## Características del Pipeline

### 1. Ingesta y Limpieza de Datos
* **Estandarización de Fechas:** Implementación de lógica compleja con Expresiones Regulares (`regexp_extract`) para unificar formatos de fecha heterogéneos provenientes de sistemas

### 2. Modelado de Datos
* Consolidación de múltiples fuentes de datos en tablas finales dentro del esquema `ddv` (Data Vault/Gold).
* Preparación de vistas consolidadas (`reclamos_provincia_consolidado`) listas para ser consumidas por herramientas de BI como Power BI o Tableau.
