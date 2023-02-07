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


* **01_Training:** datos de entrenamiento de los mapas predictores originales sin la variable X1 

* **02_Training:** datos de entrenamiento de los mapas predictores originales sin las variables X1 y X2

* **03_Training:** datos de entrenamiento transformados con PCA sin la variable X1

* **04_Training:** datos de entrenamiento transformados con PCA sin las variables X1 y X2

### Pre-requisitos 📋

_Para ejecutar los códigos en el lenguaje de programación Python se requiere un Entorno de Desarrollo Integrado (IDE). En este caso se usó la plataforma Google Collaboratory (https://colab.research.google.com/)_

### Técnicas de Aprendizaje Automático 📖

La predicción de depósitos minerales consiste en un problema de clasificación binaria, en el cual los datos tienen una etiqueta de 1 (depósito) y 0 (no-depósito). 
Para separar las clases se genera un límite de decisión que, según el número de dimensiones, puede ser un plano o hiperplano. Por excelencia los algoritmos usados para resolver tareas de clasificación son: redes neuronales artificiales, bosques aleatorios y máquinas de soporte vectorial. 



## Librerías usadas en la creación, entrenamiento y predicción de los modelos computacionales 🛠️

_Se implementaron las siguientes librerías en el desarrollo de los códigos de Python_

* [TensorFlow](https://www.tensorflow.org/?hl=es-419) - Usada para los modelos de redes neuronales artificiales y bosques aleatorios
* [Keras](https://keras.io/) - Usada para los modelos de redes neuronales artificiales
* [scikit-learn](https://rometools.github.io/rome/) - Usada para generar el modelo de máquinas de soporte vectorial

_Adicionalmente se usaron librerías especializadas para el análisis de las variables geológicas _

* [Pandas](https://pandas.pydata.org/) - Usada para cargar y filtrar los datos de entrenamiento organizados en columnas
* [Matplotlib](https://matplotlib.org/) - Usada para la visualización de superficies de decisión y gráficos estadísticos
* [Seaborn](https://seaborn.pydata.org/) - Usada para la visualización estadística de los datos
* [Numpy](https://numpy.org/) - Usada para operaciones entre vectores y matrices 

## Ejemplo en Colab 

En este Colab está un ejemplo completo del uso de las funciones y el proceso automático para aplicarlas en un archivo de excel. Para abrirlo de click en el siguiente ícono: 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](LINK DE COLAB)

FUNCIONES REPRESENTARLAS ASI <b>cal_thick</b> 










## Usarlo en el disco local

Para usar en el disco local, se debe descargar la carpeta y usar alguna de las siguientes opciones:
- Para los usuarios de Jupyter-notebook: Usar el ejemplo presentado en el archivo <b>poligonal.ipynb</b>. 
- Para los usuarios de spyder u otro IDE:  Usar el ejemplo presentado en el archivo <b>poligonal.py</b>. 

## ¿Cómo colaborar con el proyecto ? 

Ayúdame difundiendo. Envíame más ejemplos para hacer diferentes test. Encuentra errores y repórtalos en un issue en GitHub.

> Contáctanos


Ana Mantilla: anagmd2019@gmail.com </br> <a href="https://www.linkedin.com/in/ana-gabriela-mantilla-24377a21a/">
  <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="HTML tutorial" style="width:30px;height:30px;">
</a> </br> 
Paul Goyes:   goyes.yesid@gmail.com </br> <a href="https://www.linkedin.com/in/paul-goyes-0212b810/">
  <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="HTML tutorial" style="width:30px;height:30px;">
</a>
