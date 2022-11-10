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

Se comienza con la extracción de cada uno de los datasets y su análsis exploratorio. Se verificó lo siguiente: formatos, valores nulos, duplicados, estructura del dataset (filas y columnas), etiquetas de las columnas, tipo de datos en las columnas. <br>

## 2. Tranformación y normalización de los datos

En este paso se comienza con la limpieza y normalización de los datos. Se tomo como primer paso seleccionar las columnas que porporcionarian la información necesaria y reducir su dimensionalidad, a continuación se normaliza los nombres de las columnas (se cambian nombre o retiran espacios innecesarios). <br>
Se reemplazan valores nulos por etiquetas que puedan brindar mayor información en el dataset. <br>
Se cambian los formatos de tiempo y fecha, se estándarizan en caso de venir en formato diferente. Por ejemplo, 'September 17, 1908'  se cambia a '1908-09-17'. <br>
Se cambia el tipo de dato de tipo 'object' a 'int'. Para poder realziar operaciones entre las columnas  o permita su visualziación en los gráficos.
Tambien se analizan datos de las columnas y se normalizan los datos de los registros, se colocan en formatito capital o se estandarizan las etiquetas, retirando signos o datos innecesarios en las mismas, que podrian provocar una mala categorización de los datos.

*Si se detecta una operación entre columnas que podria brindar nueva información, se genera nueva columna.

## 3. Conexión a base de datos

A partir del dataframe generado en python y con el dataset transformado y normalizado se conecta al gestor de base de datos, en este caso MySQL. Se establecen las relaciones necesarias entre en los datset en caso de existir.


![image](https://user-images.githubusercontent.com/103619850/201077575-052ed2b6-e53b-415c-aa0c-49ed91c3f790.png)

Con esto se termina el proceso de EDA. Comienza el proceso de conexión entre el gestor de base de datos (MySQL) y PowerBI.
