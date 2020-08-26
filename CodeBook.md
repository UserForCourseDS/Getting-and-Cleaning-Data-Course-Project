Introducción a los datos

- Este proyecto utilizará seis datos, que son x_train.txt, x_test.txt, y_train.txt, y_test.txt, subject_train.txty subject_test.txt, todos ellos se pueden encontrar en el interior del conjunto de datos descargados, a saber URI HAR conjunto de datos .
- El archivo features.txt contiene el nombre de la variable correcta, que corresponde a cada columna de x_train.txty x_test.txt. Más explicación de cada característica está en el archivo features_info.txt.
- El archivo activity_labels.txt contiene los nombres desciptive para cada etiqueta de actividad, que corresponde a cada número en el archivo y_train.txt y el archivo y_test.txt.
- En el archivo README.txt esta la descripción general sobre el proceso general de cómo los editores de este conjunto de datos realizaron el experimento y obtuvieron el resultado de los datos.

Introducción al proyecto del curso

El script run_analysis.R usa el paquete data.table para cambiar el nombre de la columna y leer archivos. Realiza 5 pasos principales que incluyen:

- Fusiona los conjuntos de entrenamiento y prueba para crear un conjunto de datos. (A continuación, la palabra "data" significa entrenamiento y prueba). El x_data.txt, y_data.txt, subject_data.txt debe ser ordenados por fila, y después los tres deben ser ordenados por la columna.
- Extrae solo las medidas de la desviación estándar y media de cada medida. Para la columna de el archivo x_data.txt, extraiga solo los que tengan mean () o std () en sus nombres, compárelo con el archivo feature.txt.
- Utiliza nombres de actividades descriptivos para nombrar las actividades en el conjunto de datos. Haga coincidir cada número de la columna y_data con activity_labels.txt.
- Etiqueta adecuadamente el conjunto de datos con nombres de variables descriptivos. Cambie el nombre de la columna de y_datay subject_data, en lugar de usar el nombre predeterminado dado por R.
- A partir del conjunto de datos del paso 4, crea un segundo conjunto de datos ordenado e independiente con el promedio de cada variable para cada actividad y cada tema. Escribe el conjunto ordenado de datos en averagedata.txt.

Descripción final de Tidy Data

Los datos ordenados finales se producen dentro del run_analysis.R, al que se le llamo data3 y data4.

- data3 son los datos ordenados que se producen después de pasar por los primeros 4 pasos del proyecto del curso. Contiene 10299 observaciones y 68 variables.
- La primera columna se refiere a cada sujeto que hizo el experimento.
- Las columnas 2 ~ 67 son las variables de características (media y estándar de todas las variables características).
- La última columna se refiere a la actividad que estaban realizando los sujetos, incluyendo WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING.
- data4 son los datos ordenados producidos después de pasar por los 5 pasos del proyecto del curso. Contiene 180 observaciones y 68 variables. Donde la primera columna es la identificación del sujeto, la segunda columna es la actividad y el resto son el promedio de cada variable característica.
