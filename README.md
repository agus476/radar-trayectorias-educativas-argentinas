# Analítica de Riesgo de Abandono Escolar en Argentina

Proyecto de analítica aplicada que explora señales tempranas de riesgo de abandono escolar en Argentina a partir de datos históricos de matrícula, trayectoria educativa e infraestructura institucional.

El objetivo es transformar datos educativos públicos en una herramienta de lectura ejecutiva: un dashboard interactivo capaz de mostrar tendencias, segmentar perfiles críticos y sentar las bases para un futuro modelo de alerta temprana.

## Demo principal

El archivo principal del proyecto es:

- [`abandono_escolar_argentina_dashboard.ipynb`](abandono_escolar_argentina_dashboard.ipynb): notebook-dashboard con visualizaciones interactivas, narrativa ejecutiva y perfilamiento de riesgo.
- [`docs/pipeline.md`](docs/pipeline.md): explicación del flujo de datos desde archivos crudos hasta el dashboard final.

## Problema

El abandono escolar no ocurre de manera aislada ni completamente aleatoria. Puede estar asociado a señales observables como sobreedad, salidas sin pase, brechas de promoción, falta de conectividad, tipo de gestión y contexto urbano/rural.

Este proyecto analiza esas dimensiones para responder una pregunta central:

> ¿Podemos identificar perfiles institucionales con mayor riesgo educativo antes de que el abandono se consolide?

## Solución propuesta

Se construyó un flujo de trabajo de datos que integra, limpia y analiza información educativa histórica para generar un dashboard interactivo orientado a toma de decisiones.

La solución combina:

- ETL y normalización de datasets anuales.
- Tratamiento de nulos y outliers.
- Modelado e ingesta en base SQL.
- Visualizaciones interactivas con Plotly.
- Segmentación de perfiles de riesgo.
- Planteo de una futura línea de Machine Learning para alerta temprana.

## Dataset

El proyecto trabaja con bases educativas históricas de Argentina organizadas por año y temática. Las fuentes crudas se encuentran en `01_raw_data/` y los datasets consolidados iniciales están en `02_data_formatting/`.

Tablas analíticas principales:

| Dataset | Contenido | Uso analítico |
| --- | --- | --- |
| `Matricula_Secciones_Final.csv` | Matrícula, secciones, sobreedad y segmentación por provincia, departamento, sector y ámbito. | Medición de volumen, sobreedad y estructura escolar. |
| `Trayectoria_Sexo_Final.csv` | Inscritos, promovidos, no promovidos, salidas y egresos por sexo. | Análisis de retención, abandono y brecha de promoción. |
| `Establecimiento_Caracteristicas_Final.csv` | Infraestructura, conectividad, equipamiento, biblioteca y laboratorio. | Contexto institucional y recursos tecnológicos. |

## Preguntas analíticas

1. ¿La retención escolar muestra una mejora sostenida o existen señales de estancamiento?
2. ¿Cómo se comporta el flujo de retención entre niveles y años?
3. ¿Existen diferencias relevantes de promoción por sexo?
4. ¿Qué relación hay entre sobreedad y abandono?
5. ¿La infraestructura tecnológica ayuda a segmentar perfiles de riesgo?
6. ¿Qué perfiles institucionales deberían priorizarse en una futura política de alerta temprana?

## Visualizaciones principales

El dashboard final organiza el análisis en dimensiones:

- **Tendencia histórica:** evolución de salidas sin pase y tasa de abandono.
- **Brecha sociodemográfica:** flujo de retención y promoción por sexo.
- **Condición de sobreedad:** relación entre sobreedad y abandono por provincia.
- **Infraestructura escolar:** comparación de abandono según conectividad y equipamiento.
- **Perfil de riesgo:** radar de riesgo que consolida abandono, sobreedad y brecha de género.

## Hallazgos principales

- La sobreedad funciona como una señal académica relevante para perfilar riesgo de abandono.
- Las diferencias por sector, ámbito y conectividad permiten segmentar perfiles institucionales.
- El perfil **estatal / rural / sin conectividad** aparece como un segmento crítico para priorizar análisis e intervención.
- La combinación de trayectoria académica e infraestructura ofrece una base sólida para evolucionar hacia un modelo predictivo.

## Stack técnico

- Python
- Pandas
- GeoPandas
- SQLAlchemy
- PostgreSQL / Supabase
- Plotly
- HTML
- Tailwind CSS
- Jupyter / Google Colab

## Estructura del repositorio

```text
.
├── 01_raw_data/                    # Datasets crudos por año
├── 02_data_formatting/             # Concatenación y datasets consolidados
├── 03_data_cleaning/                # Limpieza general
├── 04_quality_assurance/            # QA, nulos, outliers y normalización
├── 05_database_ingestion/           # Creación de tablas e ingesta SQL
├── 06_visualization_prototype/       # Prototipo previo de visualización
├── docs/                            # Material narrativo para portfolio y charla
├── abandono_escolar_argentina_dashboard.ipynb # Dashboard final interactivo
├── requirements.txt                # Dependencias del proyecto
└── .env.example                    # Variables de entorno requeridas
```

## Configuración local

1. Crear un entorno virtual.
2. Instalar dependencias:

```bash
pip install -r requirements.txt
```

3. Configurar credenciales de base de datos usando variables de entorno. Ver `.env.example`.

## Próximo paso: Machine Learning

La siguiente evolución natural del proyecto es entrenar un modelo de clasificación para identificar instituciones con alto riesgo de abandono escolar.

Variable objetivo sugerida:

```text
alto_riesgo = 1 si una institución o segmento presenta caída fuerte de retención / egreso o tasa elevada de salidas sin pase.
alto_riesgo = 0 en caso contrario.
```

Variables candidatas:

- Tasa de abandono.
- Tasa de sobreedad.
- Brecha de promoción por sexo.
- Sector de gestión.
- Ámbito urbano/rural.
- Provincia/departamento.
- Conectividad.
- Equipamiento institucional.
- Indicadores históricos de trayectoria.

Modelos candidatos:

- Regresión logística.
- Árbol de decisión.
- Random Forest.
- Gradient Boosting.

## Nota de portfolio

Este repositorio nace de un proyecto académico y está siendo reorganizado como caso de portfolio profesional, priorizando narrativa ejecutiva, reproducibilidad, seguridad de credenciales y claridad técnica.
