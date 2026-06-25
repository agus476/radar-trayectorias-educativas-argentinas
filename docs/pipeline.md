# Pipeline del proyecto

Este repositorio conserva el flujo completo de trabajo para transformar datos educativos crudos en un dashboard analítico de riesgo de abandono escolar.

La organización usa una numeración secuencial para que el proceso sea fácil de recorrer y reproducir.

## 01_raw_data

Contiene los archivos originales por año y temática. Esta carpeta preserva la estructura de los datos fuente para mantener trazabilidad.

Incluye bases de matrícula, trayectoria, características del establecimiento, cargos y población. Algunos nombres originales pueden conservar particularidades de la fuente pública.

## 02_data_formatting

Contiene notebooks y datasets resultantes de la primera etapa de concatenación y normalización estructural.

El objetivo de esta etapa es unificar archivos anuales y producir tablas consolidadas iniciales para matrícula, trayectoria y características institucionales.

## 03_data_cleaning

Contiene datasets limpios y el notebook histórico de limpieza inicial.

Esta etapa selecciona campos relevantes, estandariza nombres, elimina columnas que no aportan al análisis y prepara variables para el modelado analítico posterior.

## 04_quality_assurance

Contiene archivos finales con tratamiento de calidad de datos.

Incluye tratamiento de nulos, revisión de outliers, normalización de texto y validaciones adicionales antes de la ingesta a base de datos.

## 05_database_ingestion

Contiene el notebook de creación de tablas e ingesta a base SQL.

Esta etapa define las tablas analíticas, genera identificadores y carga los datasets preparados para que el dashboard pueda consultar la información desde una base relacional.

## 06_visualization_prototype

Contiene el prototipo previo de visualización interactiva.

Esta etapa sirvió como base para construir el dashboard final `abandono_escolar_argentina_dashboard.ipynb`.

## Dashboard final

El archivo `abandono_escolar_argentina_dashboard.ipynb` es el entregable principal de portfolio. Integra narrativa ejecutiva, consultas SQL, visualizaciones interactivas y perfilamiento de riesgo.
