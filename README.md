# Pipeline End-to-End: Auditoría Comercial E-Commerce

## Objetivo: Unifica información comercial fragmentada (módulo de transacciones de hardware y maestro de clientes) para centralizar métricas de facturación sin depender de planillas manuales.

## Dataset: Ingesta local de dos archivos físicos (`clientes_crudo.csv` y `ventas_crudo.csv`) que simulan 50 clientes federales y 119 transacciones comerciales.

## Tecnologías
`Python` | `Pandas` | `SQLite (SQL Nativo)` | `Jupyter Notebook`

## Arquitectura de Datos y Estrategia

- **Ingesta y Normalización (Python & Pandas):** Desarrollé un pipeline automatizado para la consolidación de fuentes de datos fragmentadas (registros históricos transaccionales y maestros de clientes). El flujo realiza la limpieza, el casteo de variables numéricas y la estandarización de marcas temporales de forma eficiente.
- **Persistencia Relacional (SQLite):** Diseñé el modelo de datos e implementé la migración y persistencia automatizada de las estructuras normalizadas hacia un motor relacional en disco (`.db`).
- **Auditoría Comercial (SQL):** Creé consultas analíticas complejas utilizando integraciones relacionales avanzadas (`INNER JOIN`, `GROUP BY` y funciones de agregación) para consolidar un reporte comercial operativo automatizado, calculando métricas de facturación y el ticket promedio federal.
  

##  Estructura
* `data/` (Contiene archivos origen .csv y base de datos relacional .db)
* `analisis.ipynb` (Pipeline de procesamiento y conexión SQL)

*Nota: El repositorio contiene una muestra acotada del dataset original con fines demostrativos para el entorno de prueba local.*
