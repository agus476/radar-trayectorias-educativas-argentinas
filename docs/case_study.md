# Case Study: Analítica de Riesgo de Abandono Escolar

## Resumen

Este proyecto explora datos educativos históricos de Argentina para identificar señales tempranas de riesgo de abandono escolar. La propuesta combina datos de matrícula, trayectoria educativa e infraestructura institucional para construir un dashboard interactivo orientado a análisis y toma de decisiones.

## Contexto

El abandono escolar suele abordarse cuando el problema ya ocurrió. Este proyecto parte de una idea distinta: utilizar señales históricas y estructurales para anticipar qué perfiles institucionales pueden requerir intervención prioritaria.

## Pregunta central

¿Es posible perfilar riesgo de abandono escolar combinando trayectoria académica, sobreedad, brechas de promoción, infraestructura y contexto territorial?

## Datos utilizados

El análisis integra tres familias de datos:

1. **Matrícula y secciones:** volumen de estudiantes, secciones, sobreedad y segmentación territorial.
2. **Trayectoria por sexo:** inscritos, promovidos, no promovidos, salidas y egresos.
3. **Características del establecimiento:** conectividad, equipamiento, biblioteca, laboratorio y otros recursos institucionales.

## Metodología

El flujo de trabajo se organizó en seis etapas:

1. Recolección y organización de datasets crudos.
2. Concatenación y formateo de archivos anuales.
3. Limpieza inicial y selección de campos relevantes.
4. Tratamiento de nulos, outliers y normalización de texto.
5. Creación de tablas e ingesta en base SQL.
6. Construcción de dashboard interactivo con visualizaciones ejecutivas.

## Visualizaciones del dashboard

El dashboard se divide en cinco dimensiones:

- **Tendencia histórica:** evolución de salidas sin pase y abandono.
- **Brecha sociodemográfica:** flujo de retención y promoción por sexo.
- **Sobreedad:** relación entre sobreedad y abandono por provincia.
- **Infraestructura:** comparación entre escuelas conectadas/equipadas y sin recursos tecnológicos.
- **Perfil de riesgo:** radar que consolida abandono, sobreedad y brecha de género.

## Hallazgos clave

- La sobreedad aparece como una señal académica relevante para identificar riesgo.
- El cruce entre sector, ámbito e infraestructura permite diferenciar perfiles institucionales.
- El segmento estatal, rural y sin conectividad emerge como perfil crítico para análisis prioritario.
- La combinación de variables educativas e institucionales permite plantear una futura solución de alerta temprana.

## Valor del proyecto

El valor principal no está solo en visualizar datos históricos, sino en transformar esos datos en una herramienta analítica capaz de orientar decisiones: dónde mirar primero, qué perfiles priorizar y qué variables podrían alimentar un modelo predictivo.

## Próxima evolución

La siguiente fase consistiría en entrenar un modelo de clasificación para estimar riesgo de abandono escolar a partir de variables históricas de trayectoria, infraestructura y contexto institucional.
