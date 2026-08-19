# Pipeline End-to-End: Auditoría Comercial E-Commerce

## Objetivo: Unifica información comercial fragmentada (módulo de transacciones de hardware y maestro de clientes) para centralizar métricas de facturación sin depender de planillas manuales.

## Dataset: Ingesta local de dos archivos físicos (`clientes_crudo.csv` y `ventas_crudo.csv`) que simulan 50 clientes federales y 119 transacciones comerciales.

## Tecnologías
`Python` | `Pandas` | `SQLite (SQL Nativo)` | `Jupyter Notebook`

##  Procesoe 
* **Pandas:** Ingesta y normalización de variables numéricas y marcas temporales en memoria RAM.
* **SQLite:** Automatiza la migración de los DataFrames hacia un motor relacional en disco (`.db`).
* **SQL Pure:** Ejecuta un `INNER JOIN` con `GROUP BY` para extraer un reporte comercial ordenado por volumen de productos y cálculo automático de ticket promedio federal.

##  Estructura
* `data/` (Contiene archivos origen .csv y base de datos relacional .db)
* `analisis.ipynb` (Pipeline de procesamiento y conexión SQL)
