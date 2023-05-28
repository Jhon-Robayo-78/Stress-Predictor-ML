## Proyecto – Predictor de estrés

Realizado por:

Jonathan Javier Robayo Bossio 

Michael Andres Casadiegos Berrio

Carlos D Echeverri M

## problema 
Se plantea detectar el estrés en individuos utilizando técnicas de aprendizaje automático (NLP) en Python. Haciendo el uso de la información recolectada en subreddits de Reddit como entrada al modelo de aprendizaje, donde cada subreddit representa un patrón psicológico que puede estar asociado con el estrés. El objetivo de este problema es desarrollar un modelo preciso y efectivo para identificar el estrés en los usuarios de Reddit a partir de su actividad en los subreddits

### Etapas del Pipeline:

1.	Importación de bibliotecas: Se importan las bibliotecas necesarias, incluyendo pandas, nltk, matplotlib, seaborn y otras, para el procesamiento y análisis de datos.
2.	Descarga de recursos de NLTK: Se descargan los recursos de stopwords (palabras irrelevantes) de NLTK.
3.	Lectura de datos: Se lee un archivo CSV llamado 'Stress.csv' utilizando la función pd.read_csv() de pandas, y se guarda en un DataFrame llamado human_stress.
4.	Información del DataFrame: Se muestra información sobre las columnas y los datos en el DataFrame utilizando el método info().
5.	Análisis de valores únicos: Se cuentan los valores únicos en la columna 'subreddit' utilizando el método value_counts().
6.	Manipulación de datos: Se realizan varias operaciones en el DataFrame human_stress para agregar nuevas columnas, como calcular la longitud de los textos, mapear los valores de la columna 'label' a las etiquetas 'No Stress' y 'Stress', y extraer componentes de fecha y hora.
7.	Análisis descriptivo: Se agrupa el DataFrame por 'subreddit' y se realiza un análisis descriptivo de la longitud de los textos utilizando el método describe(), ordenando los resultados por la columna 'count'.
8.	Visualización de histogramas: Se generan histogramas de la longitud de los textos en función de la etiqueta 'No Stress' y 'Stress' utilizando el método hist() y se muestran utilizando plt.show().
9.	Visualización de gráficos de caja: Se generan gráficos de caja de la longitud de los textos en función del día de la semana utilizando sns.catplot() y se muestran utilizando plt.show().
10.	Construcción del modelo: Se dividen los datos en conjuntos de entrenamiento y prueba utilizando train_test_split(). También se define una función text_clean() para limpiar los mensajes de texto.
11.	Preparación del modelo: Se define un pipeline de procesamiento de texto y clasificación utilizando Pipeline(), que incluye etapas de vectorización de conteo de palabras, transformación tf-idf y clasificador Naive Bayes multinomial.
12.	Búsqueda de hiperparámetros: Se realiza una búsqueda de cuadrícula utilizando GridSearchCV() para encontrar los mejores hiperparámetros para el modelo.
13.	Evaluación del modelo: Se realizan predicciones en los datos de prueba utilizando el modelo optimizado y se imprime un informe de clasificación utilizando classification_report(). 
