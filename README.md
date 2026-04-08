## Propuesta 1: Evolución de la Educación en Argentina
### El enfoque:
Está centrado en el Impacto Socioeconómico y de Infraestructura en la Retención Escolar.

### Preguntas e Hipótesis:
* ¿Existe una brecha significativa en la tasa de retención y egreso entre escuelas de gestión pública versus privada, o entre escuelas urbanas versus rurales?
* ¿Se observa una disparidad de género en las tasas de egreso? De ser así, ¿esta brecha se acentúa en sectores demográficos más vulnerables?
* ¿El nivel de hacinamiento en las aulas (cantidad de alumnos por docente) tiene una correlación directa con el aumento en la deserción escolar?

### El requisito de Machine Learning:
* Opción A (Predicción de Riesgo - Clasificación): Plantear un algoritmo que, analizando la cantidad de docentes, la infraestructura del establecimiento y el historial de egresos, logre clasificar a las escuelas y detectar a tiempo cuáles tienen "alto riesgo de deserción masiva" para el año siguiente. La política pública: El Estado, al ver esa alerta del sistema, envía presupuesto de emergencia, tutores o viandas a esas escuelas específicas antes de que los chicos dejen de ir.

* Opción B (Predicción de Egresos - Regresión): Un modelo que tome todos los factores socioeducativos de una escuela y calcule exactamente cuántos alumnos se estima que van a egresar el próximo año. La política pública: Si el sistema predice una caída brusca de egresados en ciertas regiones, se proponen talleres de oficios y orientación vocacional para incentivar a los chicos de cuarto y quinto año a terminar la cursada.
  1. Talleres atados a la "Matriz Productiva" de la zona: 
Se propone que el Estado adapte los talleres a lo que necesita la industria local de esa región.
  2. Talleres de "Salida Laboral Rápida" (incentivo económico): 
Si mediante los gráficos se comprueba que las carencias del establecimiento (falta de infraestructura, zonas vulnerables) aumentan la deserción, es muy probable que esos chicos dejen la escuela porque necesitan salir a trabajar.

La propuesta: En esas escuelas específicas que marque el algoritmo, la política pública no llevaría un test vocacional clásico, sino capacitaciones en oficios cortos y muy demandados. Saber que en quinto año van a salir con un certificado en electricidad, reparación de hardware o asistencia administrativa es un incentivo gigante para que los alumnos no abandonen la cursada.
Escuelas en zonas rurales o agrícolas: Si el modelo detecta riesgo de deserción ahí, la política pública enviaría talleres de tecnología aplicada al campo, agronomía moderna o reparación de maquinaria.

Escuelas en zonas urbanas o industriales: Se implementarían talleres de oficios técnicos, armado y reparación de PC, introducción a bases de datos o programación en Python.
### Abstract:
La retención escolar y el aseguramiento del egreso en el nivel secundario representan pilares fundamentales para el desarrollo socioeconómico de Argentina. Este proyecto propone un Análisis Exploratorio de Datos (EDA) exhaustivo para evaluar cómo los factores de infraestructura, demográficos y de gestión impactan en la deserción y culminación de los estudios. Para lograrlo, implementaremos un proceso de Extracción, Transformación y Carga (ETL) que unificará múltiples conjuntos de datos públicos —incluyendo métricas de matrícula, características físicas del establecimiento, asignación de cargos docentes y trayectorias por sexo— utilizando el Código Único de Establecimiento (CUE) como clave integradora. A través de este macro-dataset y el uso de visualizaciones interactivas, buscaremos responder interrogantes estructurales: evaluaremos si existe una brecha significativa en las tasas de egreso entre escuelas de gestión pública versus privada o ámbitos urbanos versus rurales, analizaremos si el nivel de hacinamiento en las aulas (ratio alumno/docente) agrava el abandono escolar, e investigaremos posibles disparidades de género acentuadas en sectores vulnerables.

Los hallazgos de este análisis exploratorio proporcionarán la base empírica para la siguiente fase del proyecto, centrada en el desarrollo de un modelo predictivo de Machine Learning. Este algoritmo clasificatorio tendrá como objetivo identificar con anticipación aquellas instituciones que presentan un alto riesgo de caída abrupta en sus tasas de retención para el ciclo lectivo siguiente. Desde el enfoque de las políticas públicas, este sistema de alerta temprana permitirá al Estado intervenir estratégicamente y de manera preventiva, implementando talleres de formación técnica y oficios de rápida inserción laboral. Al adaptar estas capacitaciones a la matriz productiva específica de cada región demográfica, se ofrecerá un incentivo económico y vocacional tangible, reduciendo la deserción y transformando las oportunidades de los estudiantes.

## Propuesta 2: Seguridad Vial y Prevención de Accidentes
El tránsito es una de las principales causas de mortalidad en Argentina.

### El enfoque:
Analizar dónde, cuándo y por qué ocurren los accidentes para que el Estado sepa dónde poner semáforos, controles de alcoholemia o mejorar la iluminación.

### Preguntas e Hipótesis:
* ¿Existe una diferencia significativa en la tasa de letalidad (proporción de fallecidos sobre el total de lesionados) dependiendo del tipo de vehículo, siendo los motociclistas el grupo con mayor riesgo?
* ¿La severidad de los siniestros viales aumenta drásticamente durante los fines de semana en horarios de madrugada (00:00 a 06:00) en comparación con los siniestros ocurridos en días hábiles?
* ¿Representan los hombres jóvenes (entre 18 y 30 años) el grupo demográfico con mayor incidencia histórica tanto en el volumen total de lesiones como en casos fatales?

### El requisito de Machine Learning:
Plantear un modelo que, basándose en el clima, la hora y el barrio, prediga la probabilidad y gravedad de un accidente. Esto le serviría al sistema de emergencias (ambulancias/policía) para distribuir sus móviles de forma preventiva en las zonas de mayor riesgo antes de que ocurra el choque.

### Abstract:
En Argentina, la seguridad vial representa un desafío crítico para la salud pública, siendo los siniestros de tránsito una de las principales causas de mortalidad y morbilidad. En este proyecto, realizaremos un Análisis Exploratorio de Datos (EDA) utilizando un conjunto de datos públicos que abarca el período 2017-2022, el cual incluye registros detallados tanto de víctimas fatales como de lesionados a nivel nacional. Cabe destacar que, para garantizar la validez de las proyecciones y evitar sesgos analíticos, el estudio identificará y aislará la anomalía estadística correspondiente a los años 2020 y 2021, derivada del Aislamiento Social Preventivo y Obligatorio (ASPO).

El objetivo principal es comprender las dinámicas y factores subyacentes que incrementan la letalidad de estos eventos. A través de técnicas de visualización interactiva y estadística descriptiva, buscaremos responder interrogantes clave sobre la vulnerabilidad de distintos actores viales (analizando la disparidad de riesgo entre motociclistas y automóviles), definiremos el perfil demográfico de mayor siniestralidad, y mediremos la influencia directa de los fines de semana y las franjas horarias nocturnas en la gravedad de los accidentes.

Las conclusiones derivadas de este análisis sentarán las bases para una futura fase del proyecto, donde se considerará el desarrollo de un modelo predictivo de Machine Learning. Este algoritmo buscará predecir la probabilidad y severidad de los siniestros basándose en el historial de las variables contextuales mencionadas. Desde la perspectiva de las políticas públicas, la implementación de este sistema de alerta permitirá al Estado optimizar la distribución de sus recursos, reasignando controles de alcoholemia, mejorando la infraestructura y posicionando estratégicamente móviles de emergencia médica en las zonas y horarios de mayor riesgo para reducir drásticamente la tasa de mortalidad.


Datazo del Gemini:
Acordate de la regla de tu PDF: Se debe evitar utilizar datasets comunes como los relacionados con COVID-19.

Lo que NO tenés que hacer: No pongas como hipótesis principal que los accidentes bajaron mágicamente en 2020. Todo el mundo sabe que fue porque estábamos encerrados. Si centrás el trabajo en eso, el profe se los rebota.

Lo que SÍ tenés que hacer: En el análisis exploratorio (EDA), cuando muestres el gráfico de años, tenés que escribir una conclusión que diga: "Se observa una anomalía y una caída abrupta en los años 2020 y 2021, la cual descartamos como mejora estructural ya que es consecuencia directa del Aislamiento Social (ASPO). Por lo tanto, nuestro modelo predictivo le dará mayor peso al comportamiento prepandemia (2017-2019) y postpandemia (2022)."


## Propuesta 3: Salud Pública y el avance del Dengue
El Dengue es la política pública sanitaria más urgente y actual que tiene Argentina.

### El enfoque:
Ayudar al Ministerio de Salud a optimizar el presupuesto de fumigación y las campañas de descacharrado (eliminación de objetos en desuso [latas, botellas, neumáticos, baldes] que acumulan agua), entendiendo cómo se mueve el brote.

### Preguntas e Hipótesis:
* ¿Se observa una tendencia histórica en la que el pico máximo de contagios (medido en semanas epidemiológicas) se está adelantando en el calendario a medida que avanzan los años?
* ¿Existe una expansión territorial y un aumento sostenido de casos en provincias del centro o sur de Argentina (zonas históricamente no endémicas) en comparación con el norte del país?
* ¿Los años en los que el brote inicia de manera temprana (primeras semanas del año) resultan inevitablemente en un volumen anual de casos totales significativamente mayor?

### El requisito de Machine Learning:
Proponer un modelo predictivo que cruce los datos de temperatura/humedad con los casos históricos para predecir exactamente en qué semana y en qué provincia va a estallar el próximo brote, permitiendo al Estado fumigar un mes antes y salvar vidas.

### Abstract:
El Dengue se ha consolidado progresivamente como una de las emergencias epidemiológicas más urgentes y desafiantes para el sistema de salud en Argentina, presentando brotes cada vez más tempranos y expansivos a lo largo de todo el territorio nacional. Este proyecto presenta un Análisis Exploratorio de Datos (EDA) exhaustivo, fundamentado en los registros oficiales históricos de vigilancia epidemiológica, los cuales se encuentran segmentados por provincia, año y semana epidemiológica. Nuestro objetivo principal es identificar y comprender, a través del estudio de variables exclusivamente temporales y geográficas, cómo evolucionan los patrones de propagación y la magnitud de esta enfermedad transmitida por vectores.

Mediante la implementación de visualizaciones interactivas y resúmenes estadísticos detallados, buscaremos dar respuesta a interrogantes clave sobre el comportamiento del virus. En primer lugar, analizaremos si existe una tendencia histórica comprobable que evidencie un adelantamiento sistemático de los picos de contagio en el calendario anual. En segundo lugar, rastrearemos de manera geoespacial la posible expansión sostenida de los casos hacia provincias del centro o sur del país —áreas geográficas históricamente consideradas como no endémicas—. Por último, evaluaremos si aquellos años en los que el brote inicia de manera temprana resultan indefectiblemente en un volumen total de infecciones significativamente mayor.

Los patrones y hallazgos derivados de esta exploración inicial sentarán las bases empíricas sólidas para una etapa posterior y avanzada de la investigación, orientada al diseño y desarrollo de un modelo predictivo de Machine Learning. Este sistema de inteligencia artificial se entrenará utilizando las secuencias históricas de las semanas epidemiológicas y las trayectorias geográficas para anticipar con precisión la magnitud y el momento exacto de inicio de futuros brotes en cada jurisdicción. Desde el enfoque estratégico de las políticas públicas sanitarias, la adopción de este modelo predictivo como herramienta de alerta temprana permitiría al Estado optimizar drásticamente la asignación de su presupuesto. Facilitaría la planificación anticipada de campañas de prevención, la coordinación de fumigaciones focalizadas y el refuerzo oportuno de las guardias hospitalarias en las regiones de mayor riesgo, interviniendo semanas antes de que el sistema de salud alcance niveles críticos de saturación.
