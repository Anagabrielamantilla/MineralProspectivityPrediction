# Predicción de la ocurrencia de depósitos minerales tipo pórfido usando técnicas de aprendizaje automático


## Descripción del repositorio
Este es un código de Python que presenta una aplicación detallada y sistemática de los métodos de aprendizaje automático de redes neuronales
artificiales, bosques aleatorios y máquinas de soporte vectorial con el objetivo de representar el problema de predicción mineral como
un problema de clasificación con superficies de decisión.

Se realizó un flujo de preprocesamiento que incluyó la estandarización, el análisis de componentes principales y de distribución de las variables geológicas en una zona del territorio de Yukón (Canadá), donde se hizo una revisión exhaustiva de los criterios mapeables de exploración relacionados con ocurrencias minerales tipo pórfido.

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

### Resumen

El repositorio contiene los notebooks y/o códigos en Python donde se ejecutaron los análisis y los modelos de aprendizaje automático. La información está organizada de la siguiente manera:

1. Análisis preliminar de las variables explicatorias 📖

* **Gráficos de dispersión:** se analizaron las matrices de dispersión entre X1-X11. Para abrirlo acceda al archivo '01_dispersion' o de click en el siguiente ícono: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ODoKkmPzCfMmDJR9MxsphMwLP6T4iyqg#scrollTo=Uk3LzYphjYWX)

* **Matrices de correlación:** se calculó la matriz con el coeficiente de correlación de Pearson. Para abrirlo acceda al archivo '02_correlacion' o de click en el siguiente ícono: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1J-i5zozBfhTm6Xn2MeTuwR4E6xW_btVG)

2. Remoción de multicolinealidad: Análisis de componentes principales (PCA) 📖

* **PCA:** dado que el análisis de correlación indicó multicolinealidad entre las variables de entrada, se hizo una transformación a los datos con la técnica de análisis de componentes principales. Estos serán los nuevos insumos para el entrenamiento de los modelos y el cálculo de la probabilidad. Para abrirlo acceda al archivo '03_pca' o de click en el siguiente ícono: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qn98JY7233pawnWfeve0OufgNx-jsjfD#scrollTo=pt-SCkOw2qP6)


3. Técnicas de Aprendizaje Automático 📖

La predicción de depósitos minerales consiste en un problema de clasificación binaria, en el cual los datos tienen una etiqueta de 1 (depósito) y 0 (no-depósito). 
Para separar las clases se genera un límite de decisión que, según el número de dimensiones, puede ser un plano o hiperplano. Por excelencia los algoritmos usados para resolver tareas de clasificación son: 

* **Redes neuronales artificiales:** para abrirlo acceda al archivo '04_ann' o de click en el siguiente ícono:[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1RPVJYsLbxpMuZdCMuwng8fdKhc5BvfVX)

* **Bosques aleatorios:** para abrirlo acceda al archivo '05_rf' o de click en el siguiente ícono:[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1NVgu8JpfByEX-w4MUNyjwoWlWmtNP8Bk)

* **Máquinas de soporte vectorial:** para abrirlo acceda al archivo '06_svm' o de click en el siguiente ícono: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1sdXfM56fj4yaRhbNbF8qRo6O_2O3t0M4)

_Al final del entrenamiento de los modelos se evaluó la capacidad predictiva y el rendimiento del algoritmo mediante la precisión, función de pérdida, matriz de confusión, curva ROC y el valor AUC._

## Mapas de probabilidad🤓

<p align="center">
<img src="https://github.com/Anagabrielamantilla/MineralPrediction/blob/main/MapasProbabilidad.jpg" width="1000">
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
