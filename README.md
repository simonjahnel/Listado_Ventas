# Listado_Ventas
Pipeline de datos local en Python (Pandas) y SQLite para la ingesta, normalización relacional y auditoría comercial de un e-commerce tecnológico federal.

## Alcance del Proyecto
En entornos corporativos reales, los datos de clientes y transacciones suelen estar fragmentados. Este pipeline ingesta archivos CSV independientes (maestro de clientes y transacciones comerciales de hardware), automatiza la limpieza de nulos y duplicados con Pandas, y persiste la información de forma estructurada en un motor relacional local SQLite (`sqlite3`). Al final, ejecuta consultas analíticas complejas para auditar el rendimiento comercial de cada provincia.

##  Arquitectura del Proceso
1. **Simulación de Ingesta:** Carga de sets de datos crudos locales emulando el almacenamiento físico de la empresa (50 clientes federales y 119 transacciones comerciales de tecnología).
2. **ETL y Normalización (Pandas):** Parseo seguro de tipos numéricos y marcas temporales, remoción de registros defectuosos y formateo de cadenas de texto.
3. **Persistencia Relacional (SQL):** Inyección masiva automatizada de los DataFrames en tablas indexadas (`dim_clientes` y `fact_ventas`) mediante el conector nativo de SQLite.
4. **Business Intelligence (Consultas Avanzadas):** Ejecución de una consulta SQL con vinculación de entidades (`INNER JOIN`), agrupamiento geográfico (`GROUP BY c.provincia`) y funciones analíticas de control (`COUNT`, `SUM`, `AVG`).

## Métricas Extraídas del Reporte Gerencial
La consulta final genera una tabla de auditoría unificada con formato monetario local (separador de miles con punto y remoción de centavos) ordenada de mayor a menor volumen, respondiendo a tres KPIs críticos de negocio:
* **Envíos Despachados:** Volumen logístico por jurisdicción.
