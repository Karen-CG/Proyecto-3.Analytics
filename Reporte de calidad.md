# Reporte de calidad

Para cumplir con la solicitud del análisis de datos y las posibles causas que contribuyen a que sucedan los accidentes aéreos, se trabajaran con los siguientes dataset: <br>

1. AccidentesAviones.cvs : Este archivo contiene un total de 18 columnas y 5008 registros. <br>
2. AviationData.txt : Este archivo contiene un total de 32 columnas y 150952 registros. <br>( Dataset obtenido de la siguiente página https://www.ntsb.gov/Pages/Results.aspx?queryId=25cba94b-7ff0-4caa-aa48-28b542f9eca9 )

Estos dataset contienen información sobre la cantidad de personas fallecidas, tipo de aeronave, localización de los incidentes, entre otros datos relevantes. Sin embargo, la información no se encuentra normalizada para su análisis correcto; y el procesarlo directamente podría dar pauta a que se obtenga conclusiones erróneas. Por lo cual, es importante realizar la extracción, transformación y posteriormente la carga de datos a la base de datos. Al proceso descrito anteriormente lo denominaremos EDA. <br>


![EDA](https://user-images.githubusercontent.com/103619850/201061227-8f5f78b7-76fb-42da-9154-55d3fd4ae8b2.png)


Una vez realizado el EDA, podemos comenzar nuestro análsis de datos y extraer las conclusiones que respondan a los cuestionamientos o hipótesis generados. Para poder explicar a nuestra audiencia las conclusiones o hallazgos en los datos, se diseñara un dashboard que permita comprender la información que deseamos transmitir. <br>


## EDA
Se explicara de forma general los pasos realizados, para mayor detalle se puede verificar el nootbook donde se muestra el análisis y las transformaciones aplicadas en cada uno de los datasets.

## 1. Extracción y exploración de los datos

Se comienza con la extracción de cada uno de los dataset y el análsis exploratorio de cada uno de los archivos. Se verificó lo siguiente: formatos, valores nulos, duplicados, estructura del dataset (filas y columnas), etiquetas de las columnas, tipo de datos en las columnas. <br>

## 2. Tranformación y normalización de los datos

En este paso se comienza con la limpieza y normalización de los datos. Se tomo como primer paso seleccionar las columnas que porporcionarian la información necesaria y reducir la dimensionalidad, a continuación se normaliza los nombres de las columnas (se cambian nombre o retiran espacios innecesarios). <br>
Se reemplazan valores nulos por etiquetas que puedan brindar mayor información en el dataset. <br>
Se cambian los formatos de tiempo y fecha, se estándarizan en caso de venir en formato diferente. Por ejemplo, 'September 17, 1908'  se cambia a '1908-09-17'. <br>

Determinar el formato adecuado para cargar los datasets a la base de datos.
Creación de tablas en SQL y modelo de entidad relación. Verifición de buen funcionamiento de la base de datos por medio de las Query
Se realiza el proceos de carga incremental para el archivo "precios_semana_20200518.txt" y el preprocesamienyo del archivo antes de ser cargado a la base datos.
Se verifica nuevamente el funcionamiento de la base de datos.
