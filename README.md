# Analisis de Viajes en Taxi y Efecto del-Clima

Como analista de datos para Zuber, una nueva empresa de viajes compartidos que busca lanzarse en Chicago, desarrollé un proyecto de análisis integral con el objetivo de comprender las preferencias de los pasajeros y el impacto de factores externos en la frecuencia y duración de los viajes.

# 1. Preparación y Exploración de Datos

Primero, trabajé con la base de datos histórica de viajes en taxi de Chicago y con registros meteorológicos del mes de noviembre de 2017. Esto implicó:

Importación y limpieza de datos de las tablas neighborhoods, cabs, trips y weather_records.

Validación de los tipos de datos y estandarización de los timestamps para poder relacionar viajes con condiciones climáticas.

Generación de un dataset consolidado que permitiera cruzar información de viajes con datos de clima utilizando las horas de inicio de los trayectos.

# 2. Análisis Exploratorio en SQL

Realicé varias consultas SQL para obtener insights iniciales:

Calculé el número de viajes por compañía de taxis durante el 15 y 16 de noviembre de 2017, identificando las empresas con mayor actividad.

Filtré las compañías que contenían en su nombre las palabras “Yellow” o “Blue”, para conocer su participación en el mercado durante la primera semana de noviembre.

Clasifiqué a las empresas de taxis en tres grupos: Flash Cab, Taxi Affiliation Services y Other, determinando que las dos primeras concentraban la mayoría de viajes en noviembre.

# 3. Cruce de Datos con Condiciones Meteorológicas

Identifiqué los viajes desde el Loop (neighborhood_id 50) hasta O’Hare (neighborhood_id 63) que ocurrieron los sábados de noviembre.

Clasifiqué las condiciones meteorológicas en dos categorías: Good (sin lluvia ni tormenta) y Bad (con lluvia o tormenta).

Generé un dataset final con la duración de los viajes y la condición climática correspondiente, excluyendo aquellos sin datos de clima.

# 4. Análisis en Python y Visualización

Importé los resultados en Python y realicé un análisis exploratorio de los datos.

Identifiqué los 10 barrios con mayor número de viajes de finalización en noviembre de 2017 y construí visualizaciones comparativas.

Generé gráficos de barras que mostraron:

Distribución de viajes por empresa de taxis.

Ranking de los principales barrios en número de viajes finalizados.

A partir de los gráficos, concluí que la demanda de taxis está altamente concentrada en ciertas zonas y en unas pocas empresas dominantes, lo que puede influir en la estrategia de posicionamiento de Zuber.

# 5. Prueba de Hipótesis

Finalmente, probé la hipótesis:

H₀: La duración promedio de los viajes del Loop a O’Hare es la misma los sábados con lluvia y sin lluvia.
H₁: La duración promedio de los viajes cambia en los sábados lluviosos.

Utilicé una prueba estadística de hipótesis (t-test para dos muestras independientes) con un nivel de significación α = 0.05.
Los resultados indicaron si la diferencia observada era estadísticamente significativa, lo que permitió concluir si el clima afecta o no la duración de los viajes en este trayecto clave.

# Conclusiones Generales

Las empresas Flash Cab y Taxi Affiliation Services lideran el mercado de taxis en Chicago, por lo que Zuber deberá competir principalmente con ellas.

La distribución de la demanda es desigual: pocos barrios concentran la mayoría de viajes, lo que sugiere que las campañas de lanzamiento deben priorizar estas zonas.

El análisis estadístico permitió cuantificar el efecto del clima en la duración de los viajes, información clave para diseñar estrategias de precios dinámicos y mejorar la experiencia del usuario.
