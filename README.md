
<p align="center"><h1>PROYECTO INDIVIDUAL 2: SINIESTROS VIALES:warning:</h1></p> 


*<h3>INTRODUCCIÓN:</h3>*
En este proyecto se simula el rol de un Data Analyst que forma parte del equipo de analistas de datos de una empresa consultora a la cual el Observatorio de Movilidad y Seguridad Vial (OMSV) , que es un centro de estudios que se encuentra bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires (CABA), le solicitó la elaboración de un proyecto de análisis de datos, con el fin de generar información que le permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales. Para ello, se puso a disposición un dataset sobre homicidios en siniestros viales acaecidos en la Ciudad de Buenos Aires durante el periodo 2016-2021.
Como mínimos entregables, se espera un análisis exploratorio de datos, metodologías adoptadas, análisis de KPIs y principales conclusiones, como así también un dashboard acorde.

*<h3>CONTEXTO:</h3>*
Los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, son eventos que involucran vehículos en las vías públicas. Pueden tener diversas causas, como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos o caídas de vehículos. Estos incidentes pueden resultar en consecuencias que van desde daños materiales hasta lesiones graves o fatales para los involucrados.
En Argentina, cada año mueren cerca de 4.000 personas en siniestros viales. Entre 2018 y 2022 se registraron 19.630 muertes en siniestros viales en todo el país. Sólo en la Ciudad Autónoma de Buenos Aires, en el año 2022, fueron 103 víctitmas. Estos datos se pueden ver en el siguiente [Link](https://luchemos.org.ar/es/estadisticas/muertosanuales)

*<h3>DATOS:</h3>*
Se analizó el conjunto de datos denominado "Homicidios", que contiene los apartedos "Hechos" y "Víctimas" de la página del Gobierno de la Ciudad. [Link](https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales)
El apartado de "Hechos" contiene Id único del suceso, fecha en la que se produjo, la locación, y el rol de los participantes.
Por otra parte, el apartado "Víctimas" contiene datos sobre las mismas, como edad, sexo, y modo de desplazamiento; como así también el Id del hecho.
Además, se ingresó otro dataset de la página del Gobierno de la Ciudad, para ver a qué barrios correspondía cada comuna [Link](https://buenosaires.gob.ar/sindicatura/universo-de-control/comunas-15)
Posteriormente, se sacaron los datos oficiales de los censos 2010 y 2022 para establecer la cantidad de habitantes de la Ciudad Autónoma de Buenos Aires [Link](https://censo.gob.ar/index.php/datos_definitivos_caba)

*<h3>ANÁLISIS:</h3>*
Para la elaboración de este proyecto se utilizó Python y Pandas para los procesos de extracción, transformación y carga de los datos, como así también para el análisis exploratorio de los datos, en cuyo caso también se utilizó matplotlib y seaborn.
Para la construcción de un dashboard interactivo se utilizó Power BI.
Asimismo, se utilizó el 'Manual de normas / Identidad Visual Institucional' del Gobierno de la Ciudad, para extraer y utilizar la paleta cromática. [Link](https://cdn2.buenosaires.gob.ar/gestiondigital/Manual%20GCBA%20Versi%C3%B3n%20Final..pdf)

Como primera medida, se realizó un análisis según las víctimas, su sexo y edad, como así también por rol y transporte. Se observa que el 77% de las víctimas son masculinas, teniendo un pico en el rango etario de 35-44.
De acuerdo al rol de la víctima, aproximadamente el 45% era conductor. Teniendo en cuenta el transporte, un 42% estaba a bordo de una motocicleta.

Luego se analizó la variable temporal, para entender la distribución de los homicidios en distintas escalas temporales. Casi el 61% de los accidentes se produjeron entre los años 2016 y 2018. Luego se ve una baja en el 2019, 2020 y 2021. Por otra parte, el mes que mayor cantidad de víctimas tiene es el mes de diciembre. Además, los días lunes son el día con mayor cantidad de accidentes, y si hablamos de rango horario, de 06:00 a 09:00hs.

Por último, se realizó un análisis por zona, donde se puede observar que el 62% de los accidentes se produjo en avenidas, y el 75% fue en cruce de calles. Además, se observa que la Comuna que más accidentes tiene es la Comuna 1, que consta de los barrios Retiro, San Nicolás, Puerto Madero, San Telmo, Montserrat y Constitución.

*<h3>KPIs:</h3>*
se plantearon tres objetivos en relación a la disminución de la cantidad de víctimas fatales de los siniestros viales, desde los cuales se proponen tres indicadores de rendimiento clave o KPI.

Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior

Las tasas de mortalidad relacionadas con siniestros viales suelen ser un indicador crítico de la seguridad vial en una región. Se define como Tasa de homicidios en siniestros viales al número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico, en este caso se toman 6 meses. Su fórmula es:

ú
ó
 

Como Población Total se calculó la población para el año 2021 a partir de los censos poblacionales del año 2010 y 2022.

En este caso, para el año 2021, la Tasa de homicidios en siniestros viales fue de 1.77 lo que significa que, durante los primeros 6 meses del año 2021, hubo aproximadamente 1.77 homicidios en accidentes de tránsito por cada 100,000 habitantes. Ahora, el objetivo planteado es reducir esta tasa para el siguiente semestre de 2021 en un 10%, esto es 1.60. Cuando se calcula el KPI para este período se obtiene que la Tasa de homicidios en siniestros viales fue de 1.35, lo que significa que para el segundo semestre de 2021 se cumple con el objetivo propuesto.

Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior

Como se vio en el análisis exploratorio, el 42% de las víctimas mortales se transportaban en moto al momento del hecho. Por lo que se consideró importante proponer el monitoreo de la cantidad de accidentes mortales en este tipo de conductor. Para ello se define a la Cantidad de accidentes mortales de motociclistas como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban en moto en un determinado periodo temporal. La fórmula para medir la evolución de los accidentes mortales con víctimas en moto es:

íñíñ
íñ
 

Donde:

íñ
: Número de accidentes mortales con víctimas en moto en el año anterior
íñ
: Número de accidentes mortales con víctimas en moto en el año actual
Para este caso, se toma como año actual al año 2021 y como año anterior al año 2020. En primer lugar, se calculó la Cantidad de accidentes mortales de motociclistas para el año 2020, el cual resultó de -44.00, de esta manera el objetivo a cumplir es de -40.92 (es decir, la reducción del 7% de la cantidad de accidentes para 2020). El calcular la Cantidad de accidentes mortales de motociclistas para el año 2021 resultó de 64.29 lo que significa que aumentó un 64% la cantidad de muertes de conductores de motociclistas respecto del 2021.

Reducir en un 10% la tasa de homicidios en las avenidas en el último año, en CABA, respecto al año anterior

Como se vio en el análisis exploratorio, el 62% de las víctimas mortales transitaban por avenidas al momento del hecho. Se define a la Tasa de homicidios en las avenidas al número de víctimas fatales en accidentes de tránsito en avenidas por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico, en este caso anual. Su fórmula es:

úí
ó
 

En primer lugar se calculó la Tasa de homicidios en las avenidas para el año 2020, la cual resultó en 1.68. De esta se pudo determinar el objetivo a cumplir al año siguiente, que resultó en 1.51 (es decir, la reducción del 10% de la tasa de homicios respecto del 2020). Finalmente, al calcular la Tasa de homicidios en las avenidas para el año 2021, la misma resultó de 1.97, lo que significa que se superó el objetivo, aumentando la tasa de mocidios en avenidas respecto al año anterior.
