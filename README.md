# Predicción de la ocurrencia de depósitos minerales tipo pórfido usando técnicas de aprendizaje automático


## Descripción del repositorio
Este es un código de Python que presenta una aplicación detallada y sistemática de los métodos de aprendizaje automático de redes neuronales
artificiales, bosques aleatorios y máquinas de soporte vectorial con el objetivo de representar el problema de predicción mineral como
un problema de clasificación con superficies de decisión.

Se realizó un flujo de preprocesamiento que incluyó la estandarización, el análisis de componentes principales y de distribución de las variables geológicas en una zona del territorio de Yukón (Canadá), donde se hizo una revisión exhaustiva de los criterios mapeables de exploración relacionados con ocurrencia minerales tipo pórfido.

Los resultados obtenidos indican que la incorporación del aprendizaje automático en el flujo de trabajo de exploración mineral supone una mejora considerable en la optimización de recursos y el grado de confiabilidad en los objetivos de exploración. 

## Base de datos 📋

_Todos los datos usados en este repositorio son de libre acceso y se encuentran en la página del Servicio Geológico de Yukón (https://data.geology.gov.yk.ca/) y el Gobierno de Canadá (https://www.canada.ca/en.html)._

La información está organizada de la siguiente forma: 

* **00_Training:** corresponde a un muestreo de datos extraído de once mapas predictores que representan: 

           📌 X1 : Proximidad a rocas plutónicas

           📌 X2: Proximidad a rocas volcánicas

           📌 X3: Proximidad a fallas geológicas

           📌 X4: Proximidad a contactos de terrenos litotectónicos

           📌 X5: Valores del campo total magnético residual

           📌 X6: Valores de la primera derivada vertical del campo total magnético residual

           📌 X7: Concentración geoquímica de Zn 

           📌 X8: Concentración geoquímica de Au

           📌 X9: Concentración geoquímica de Cu 

           📌 X10: Concentración geoquímica de Mo 

           📌 X11: Concentración geoquímica de Pb 

           🚀 DEP: Columna con las etiquetas de depósito (1) y no-depósito (0)

* **04_Training:** datos de entrenamiento transformados con PCA sin las variables X1 y X2

* **04_Virtual_Raster:** esta capa contiene once bandas. Cada una corresponde a un componente principal extraído de las variables X3-X11.Con este archivo se realiza la predicción del mapa de probabilidad. Para descargarlo acceder al siguiente enlace https://correouisedu-my.sharepoint.com/:f:/g/personal/ana_mantilla_correo_uis_edu_co/EnBcbDu57E9EisK3jZRr4ZwBbPvP2Cky9V2F4OLhdWDLvg?e=d8XHLc

### Pre-requisitos 📋

_Para ejecutar los códigos en el lenguaje de programación Python se requiere un Entorno de Desarrollo Integrado (IDE). En este caso se usó la plataforma Google Collaboratory (https://colab.research.google.com/)_

### Análisis preliminar de las variables explicatorias 📖

* **Superficies de decisión:** En este Colab está un ejemplo completo de la visualización de los datos. Este paso es importante para determinar los factores condicionantes que pueden resultar desfavorables para la implementación de los algoritmos computacionales. En este caso se analizaron matrices de dispersión entre X1-X11. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ODoKkmPzCfMmDJR9MxsphMwLP6T4iyqg#scrollTo=Uk3LzYphjYWX)

* **Matrices de correlación:** En este Colab está un ejemplo completo del cálculo de coeficiente de correlación de Pearson para el análisis de correlación entre las variables de entrada. En este caso se observó que los datos estaban altamente correlacionados, por lo cual se aplicó el análisis de componentes principales para remover la multicolinealidad. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1J-i5zozBfhTm6Xn2MeTuwR4E6xW_btVG)


### Técnicas de Aprendizaje Automático 📖

La predicción de depósitos minerales consiste en un problema de clasificación binaria, en el cual los datos tienen una etiqueta de 1 (depósito) y 0 (no-depósito). 
Para separar las clases se genera un límite de decisión que, según el número de dimensiones, puede ser un plano o hiperplano. Por excelencia los algoritmos usados para resolver tareas de clasificación son: redes neuronales artificiales, bosques aleatorios y máquinas de soporte vectorial. 

<p align="center">
<img src="https://github.com/Anagabrielamantilla/MineralPrediction/blob/main/Fig7_Metodologia - copia.png" width="500">
</p>


## Librerías usadas en la creación, entrenamiento y predicción de los modelos computacionales 🛠️

_Se implementaron las siguientes librerías en el desarrollo de los códigos de Python_

* [TensorFlow](https://www.tensorflow.org/?hl=es-419) - Usada para los modelos de redes neuronales artificiales y bosques aleatorios
* [Keras](https://keras.io/) - Usada para los modelos de redes neuronales artificiales
* [scikit-learn](https://rometools.github.io/rome/) - Usada para generar el modelo de máquinas de soporte vectorial

_Adicionalmente se usaron librerías especializadas para el análisis de las variables geológicas_

* [Pandas](https://pandas.pydata.org/) - Usada para cargar y filtrar los datos de entrenamiento organizados en columnas
* [Matplotlib](https://matplotlib.org/) - Usada para la visualización de superficies de decisión y gráficos estadísticos
* [Seaborn](https://seaborn.pydata.org/) - Usada para la visualización estadística de los datos
* [Numpy](https://numpy.org/) - Usada para operaciones entre vectores y matrices 

## Ejemplo de los modelos en Colab⌨️

* **Modelo de redes neuronales artificiales:** En este Colab está un ejemplo completo del modelo de redes neuronales artificiales. Para abrirlo de click en el siguiente ícono: 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1RPVJYsLbxpMuZdCMuwng8fdKhc5BvfVX)

* **Modelo de bosques aleatorios:** En este Colab está un ejemplo completo del modelo de bosques aleatorios
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1NVgu8JpfByEX-w4MUNyjwoWlWmtNP8Bk)

* **Modelo de máquinas de soporte vectorial:** En este Colab está un ejemplo completo del modelo de máquinas de soporte vectorial
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1sdXfM56fj4yaRhbNbF8qRo6O_2O3t0M4)


_Al final del entrenamiento de los modelos se evaluó la capacidad predictiva y el rendimiento del algoritmo mediante la precisión, función de pérdida, matriz de confusión, curva ROC y el valor AUC._


## Mapas de probabilidad🤓

<p align="center">
<img src="https://github.com/Anagabrielamantilla/MineralPrediction/blob/main/MapasProbabilidadjpeg.jpg" width="2000">
</p>

## ¿Cómo colaborar con el proyecto ? 

Ayúdame difundiendo. Encuentra errores y repórtalos en un issue en GitHub. También puedes contactarnos por medio de nuestras redes sociales.


## Autores ✒️

* **Ana Gabriela Mantilla:** anagmd2019@gmail.com </br> <a href="https://www.linkedin.com/in/ana-gabriela-mantilla-24377a21a/">
  <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="HTML tutorial" style="width:30px;height:30px;">
</a> </br> 
* **Paul Goyes:**   goyes.yesid@gmail.com </br> <a href="https://www.linkedin.com/in/paul-goyes-0212b810/">
  <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="HTML tutorial" style="width:30px;height:30px;">
</a>
