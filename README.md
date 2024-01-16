
<p align="center"><h1>PROYECTO INDIVIDUAL 2: SINIESTROS VIALES :warning:</h1></p> 


*<h3>:yellow_square: INTRODUCCIÓN:</h3>*
En este proyecto se simula el rol de un Data Analyst que forma parte del equipo de analistas de datos de una empresa consultora a la cual el Observatorio de Movilidad y Seguridad Vial (OMSV) , que es un centro de estudios que se encuentra bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires (CABA), le solicitó la elaboración de un proyecto de análisis de datos, con el fin de generar información que le permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales. Para ello, se puso a disposición un dataset sobre homicidios en siniestros viales acaecidos en la Ciudad de Buenos Aires durante el periodo 2016-2021.
Como mínimos entregables, se espera un análisis exploratorio de datos, metodologías adoptadas, análisis de KPIs y principales conclusiones, como así también un dashboard acorde.

*<h3>:yellow_square: CONTEXTO:</h3>*
Los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, son eventos que involucran vehículos en las vías públicas. Pueden tener diversas causas, como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos o caídas de vehículos. Estos incidentes pueden resultar en consecuencias que van desde daños materiales hasta lesiones graves o fatales para los involucrados.
En Argentina, cada año mueren cerca de 4.000 personas en siniestros viales. Entre 2018 y 2022 se registraron 19.630 muertes en siniestros viales en todo el país. Sólo en la Ciudad Autónoma de Buenos Aires, en el año 2022, fueron 103 víctitmas. Estos datos se pueden ver en el siguiente [Link](https://luchemos.org.ar/es/estadisticas/muertosanuales)

*<h3>:yellow_square: DATOS:</h3>*
Se analizó el conjunto de datos denominado "Homicidios", que contiene los apartedos "Hechos" y "Víctimas" de la página del Gobierno de la Ciudad. [Link](https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales)
El apartado de "Hechos" contiene Id único del suceso, fecha en la que se produjo, la locación, y el rol de los participantes.
Por otra parte, el apartado "Víctimas" contiene datos sobre las mismas, como edad, sexo, y modo de desplazamiento; como así también el Id del hecho.
Además, se ingresó otro dataset de la página del Gobierno de la Ciudad, para ver a qué barrios correspondía cada comuna [Link](https://buenosaires.gob.ar/sindicatura/universo-de-control/comunas-15)
Posteriormente, se sacaron los datos oficiales de los censos 2010 y 2022 para establecer la cantidad de habitantes de la Ciudad Autónoma de Buenos Aires [Link](https://censo.gob.ar/index.php/datos_definitivos_caba)

*<h3>:yellow_square: ANÁLISIS:</h3>*
Para la elaboración de este proyecto se utilizó Python y Pandas para los procesos de extracción, transformación y carga de los datos, como así también para el análisis exploratorio de los datos, en cuyo caso también se utilizó matplotlib y seaborn.
Para la construcción de un dashboard interactivo se utilizó Power BI.
Asimismo, se utilizó el 'Manual de normas / Identidad Visual Institucional' del Gobierno de la Ciudad, para extraer y utilizar la paleta cromática. [Link](https://cdn2.buenosaires.gob.ar/gestiondigital/Manual%20GCBA%20Versi%C3%B3n%20Final..pdf)

Como primera medida, se realizó un análisis según las víctimas, su sexo y edad, como así también por rol y transporte. Se observa que el 77% de las víctimas son masculinas, teniendo un pico en el rango etario de 35-44.
De acuerdo al rol de la víctima, aproximadamente el 45% era conductor. Teniendo en cuenta el transporte, un 42% estaba a bordo de una motocicleta.

![image](https://github.com/camillaneza/PI2_Siniestros_Viales/assets/109699708/025a0812-3394-4bc5-a244-66028eb89e75)

![image](https://github.com/camillaneza/PI2_Siniestros_Viales/assets/109699708/26f0c6e1-45b6-4247-a73d-7411e01cf1fc)


Luego se analizó la variable temporal, para entender la distribución de los homicidios en distintas escalas temporales. Casi el 61% de los accidentes se produjeron entre los años 2016 y 2018. Luego se ve una baja en el 2019, 2020 y 2021. Por otra parte, el mes que mayor cantidad de víctimas tiene es el mes de diciembre. Además, los días lunes son el día con mayor cantidad de accidentes, y si hablamos de rango horario, de 06:00 a 09:00hs.


![image](https://github.com/camillaneza/PI2_Siniestros_Viales/assets/109699708/0598e5cc-5240-4365-9031-69adafa80a9c)

![image](https://github.com/camillaneza/PI2_Siniestros_Viales/assets/109699708/76719af8-8e09-4a5b-8d1b-2897bd868918)


Por último, se realizó un análisis por zona, donde se puede observar que el 62% de los accidentes se produjo en avenidas, y el 75% fue en cruce de calles. Además, se observa que la Comuna que más accidentes tiene es la Comuna 1, que consta de los barrios Retiro, San Nicolás, Puerto Madero, San Telmo, Montserrat y Constitución.

![image](https://github.com/camillaneza/PI2_Siniestros_Viales/assets/109699708/dd408041-7bce-44a1-9d0f-41428fcb6532)

![image](https://github.com/camillaneza/PI2_Siniestros_Viales/assets/109699708/fd07f9ad-f1d6-4954-ac18-ef1dea1dd87e)

*<h3>:yellow_square: KPIs:</h3>*
Se plantearon tres objetivos en relación a la disminución de la cantidad de víctimas fatales de los siniestros viales, desde los cuales se proponen tres indicadores de rendimiento clave o KPI.

:yellow_circle: Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior .

Definimos a la tasa de homicidios en siniestros viales como el número de víctimas fatales en accidentes de tránsito por cada 100.000 habitantes en un área geográfica durante un período de tiempo específico. Su fórmula es: (Número de homicidios en siniestros viales / Población total) * 100,000

En el contexto del primer semestre del año 2021, la tasa de homicidios en siniestros viales fue de 1.77., es decir que se registraron aproximadamente 1.77 homicidios en accidentes de tránsito por cada 100,000 habitantes. Al calcular la tasa de homicidios viales para el segundo semestre de ese año, se pudo apreciar que fue del 1.35. Por lo tanto, se logró cumplir con la meta propuesta indicada precedentemente.


:yellow_circle: Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior .

Definimos a la cantidad de accidentes mortales de motociclistas en siniestros viales como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaron en moto en un determinado periodo temporal. Su fórmula para medir la evolución de los accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en moto en el año actual - Número de accidentes mortales con víctimas en moto en el año anterior) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100

En este caso, se calculó la Cantidad de accidentes mortales de motociclistas para el año 2020 (año anterior), el cual resultó de -44.00, de esta manera el objetivo a cumplir es de -40.92. Al momento de calcular la cantidad de accidentes mortales de motociclistas para el año 2021 resultó de 64.29 lo que significa que aumentó un 64% la cantidad de muertes de conductores de motociclistas respecto del 2021. Por lo tanto, no se logró cumplir con la meta propuesta indicada precedentemente.


:yellow_circle: Reducir en un 10% la cantidad de accidentes mortales producidos en el último año, en cruce de calles, en CABA, respecto al año anterior. Se define al número de víctimas fatales en accidentes de tránsito en cruce de calles por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico, en este caso anual.(Número de accidentes mortales de víctimas en cruce de calles / Población total) *100,000

En el año 2020 (año anterior), la tasa de accidentes mortales producidos en cruce de calles fue de 2.03, es decir que se registraron aproximadamente 2.03 homicidios en accidentes de tránsito por cada 100,000 habitantes. Al calcular la tasa para el año actual, es decir 2021, se pudo apreciar que fue del 2.13. Por lo tanto, no se logró cumplir con la meta propuesta indicada precedentemente.
 

![image](https://github.com/camillaneza/PI2_Siniestros_Viales/assets/109699708/27e4b817-5cc3-4f7b-823f-9814fa653d4b)

*<h3>:yellow_square: CONCLUSIONES:</h3>*
En el periodo comprendido entre 2016 y 2021, se produjeron 717 homicidios por siniestros viales en la Ciudad Autónoma de Buenos Aires. Casi el 61% de los accidentes se produjeron entre los años 2016 y 2018. Luego se ve una baja en el 2019, 2020 y 2021. Por otra parte, el mes que mayor cantidad de víctimas tiene es el mes de diciembre. Además, los días lunes son el día con mayor cantidad de accidentes, y si hablamos de rango horario, de 06:00 a 09:00hs.
Por otra parte, se observa que el 77% de las víctimas son masculinas, teniendo un pico en el rango etario de 35-44. Aproximadamente el 45% era conductor, y un 42% estaba a bordo de una motocicleta.
El 62% de los accidentes se produjo en avenidas, y el 75% fue en cruce de calles. Además, se observa que la Comuna que más accidentes tiene es la Comuna 1, que consta de los barrios Retiro, San Nicolás, Puerto Madero, San Telmo, Montserrat y Constitución.
Se logró alcanzar la meta de reducir la tasa de homicidios en siniestros viales para el segundo semestre de 2021, pero los objetivos de disminuir la cantidad de accidentes mortales en motociclistas y en cruce de calles para el año 2021, en comparación con 2020, no fueron cumplidos.

*<h3>:yellow_square: RECOMENDACIONES:</h3>*
 :small_blue_diamond: Reforzar controles los días de semana en el rango horario antedicho. 

:small_blue_diamond: Reforzar controles de motociclistas, como así también exigir el uso del casco de protección obligatorio.

:small_blue_diamond: Reforzar controles en avenidas.

:small_blue_diamond: Reforzar controles y añadir semáforos en cruces de calles, y especialmente, en la Comuna 1.

:small_blue_diamond: Realizar campañas de concientización especialmente para Hombres
