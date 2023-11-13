# Modelo de Clasificación para Hospitalización de Pacientes Sometidos a Biopsia Prostática

## Planteamiento de la Problemática

Este proyecto tiene como objetivo identificar las características más relevantes de los pacientes que, tras someterse a una biopsia prostática, experimentan hospitalización. Se define como **caso** aquel paciente que, en un plazo máximo de 30 días después del procedimiento, presenta fiebre, infección urinaria o sepsis, requiriendo manejo médico ambulatorio u hospitalario para resolver la complicación. Por otro lado, se designa como **control** al paciente sometido a biopsia prostática que no presenta complicaciones infecciosas en los 30 días siguientes.

## Datos Disponibles

Con el fin de lograr la clasificación de pacientes hospitalizados o no, se cuenta con una base de datos que consta de 570 registros y 20 variables para su análisis. Estos datos abarcan aspectos como `Antecedentes del paciente`, `Morbilidad asociada al paciente`, `Antecedentes relacionados con la toma de la biopsia` y `Complicaciones infecciosas`.

## Procesamiento de los Datos

A través de un proceso de Extracción, Transformación y Carga (ETL), se consumieron los datos proporcionados, convirtiéndolos en un DataFrame. Se llevó a cabo una exploración y limpieza inicial, transformación de los datos y carga del conjunto limpio. Posteriormente, mediante un Análisis Exploratorio de Datos (EDA), se exploraron las variables con el objetivo de comprender su naturaleza y establecer relaciones con la variable objetivo. Durante esta exploración, se descartaron algunas variables para preparar los datos en un formato compatible para la modelación del problema.

## Modelo de Clasificación

Una vez preparados los datos, se procedió a seleccionar un modelo de Machine Learning de clasificación capaz de categorizar a un paciente como *hospitalizado* o *no hospitalizado*. Se plantearon dos estrategias: la primera utilizando las 12 columnas de datos y la segunda considerando la reducción de dimensionalidad. Ambas estrategias emplearon los algoritmos de Árbol de Decisión, K-Vecinos Cercanos y Máquina de Soporte de Vectores. La elección de los mejores hiperparámetros se realizó mediante una búsqueda exhaustiva utilizando la técnica de GridSearch.

## Conclusiones

Se logró desarrollar un modelo de clasificación efectivo que permite determinar la probabilidad de hospitalización de un paciente a partir de sus antecedentes, incluyendo factores como la edad, la intervención de biopsia y la morbilidad general. El modelo más destacado fue un Árbol de Decisión con una profundidad máxima de 19 y criterio de decisión Gini. Previo a esto, se aplicó una reducción de dimensionalidad utilizando PCA, donde se determinaron 8 componentes como la mejor opción. La métrica de evaluación utilizada fue el F1 Score (Test_F1), obteniendo un rendimiento aceptable de 0.77, considerando el desbalance de la clase objetivo.




## Autor ✒️
* **Osvaldo Gabriel Sosa**  - [LinkedIn](https://www.linkedin.com/in/gabriel-sosa26)