![](logo.png)

# Unidad: Dimensionalidad y Agrupación - Sesión 2

## Reducción de dimensiones en Machine Learning

* Para poder realizar esta actividad debes haber revisado la lectura correspondiente a la semana.
* Crea una carpeta de trabajo y guarda todos los archivos correspondientes (notebook y csv).
* Una vez terminada la actividad, comprime la carpeta y sube el `.zip` a la sección correspondiente.


## Ejercicio 1: Preparación del ambiente de trabajo

* Para este ejercicio trabajaremos de manera __conjunta__ en dos bases de datos que se encuentra en `sklearn.datasets`:
    * `breast_cancer`: Base de datos de diagnóstico de cáncer de mamas.
    * `iris`: Base de datos sobre atributos morfológicos de flores _Iris_.

* Importe los módulos básicos para el análisis de datos.
* Importe los módulos `KMeans`, `PCA`, `train_test_split` y `StandardScaler`.


## Ejercicio 2: Agrupando atributos con KMeans

* Importe la base de datos `iris` con `load_iris` en un nuevo objeto:
    - _tip_: La matriz de atributos se encuentra en `.data`.
* Para simplificar la dimensionalidad de la base reduzca las dimensiones de la base de datos para obtener dos componentes principales.
* Comente cuánta es la varianza explicada por ambos componentes.
* Grafique ambas dimensiones con un scatter plot.
* Exploremos la cantidad de clusters necesarios. Para ello estimen la inercia con $k$ entre 2 y 50. También calculen el diferencial (_tip_: puede utilizar el método `.diff()` de `pd.Series`). Grafiquen ambas curvas.
* Utilicen como criterio de selección aquél cluster cuya disminución en la inercia sea mayor a 15.
* Reentrenen el modelo con todos los datos en base al criterio de selección.
* Grafique los resultados e identifique todos los puntos con `kmeans.labels_`


## Ejercicio 2: Reduciendo dimensiones

* Importe la base de datos `breast_cancer` con `load_breast_cancer` en un nuevo objeto:
    - _tip_: La matriz de atributos se encuentra en `.data`.
* Separe los datos en dos objetos: `benigno` y `maligno`. Utilice la información disponible en `.target` para ello.
* Ahora compararemos la distribución empírica para cada atributo en la base mediante histogramas.
* Reduzca la matriz de atributos a dos.
* Reporte el nivel de de varianza explicada por ambas dimensiones.
* Reporte la asociación entre cada atributo y los componentes extraídos.
* Visualice la relación entre ambos componentes y etiquete los puntos en base a su atributo `target`.


