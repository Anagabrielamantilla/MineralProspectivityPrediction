[![DOI](https://zenodo.org/badge/475663279.svg)](https://zenodo.org/badge/latestdoi/475663279)


# Predicción de la ocurrencia de depósitos minerales tipo pórfido usando técnicas de aprendizaje automático


## Descripción del repositorio

Este repositorio tiene códigos en Python que predicen la probabilidad de ocurrencia mineral en una zona del territorio de Yukón (Canadá) usando redes neuronales
artificiales, bosques aleatorios y máquinas de soporte vectorial. Este proyecto hace parte de uno de los resultados de mi tesis de pregrado, cuyas diapositivas se encuentran en [este link](https://correouisedu-my.sharepoint.com/:b:/g/personal/ana_mantilla_correo_uis_edu_co/EZV-gR6sAy5DpEWUlqelyn0BGEdKJj_XzEbV-5OfGJtnEQ?e=zhl2n9)

## Base de datos 📋

Todos los datos usados en este repositorio son de libre acceso y se encuentran en la página del [Servicio Geológico de Yukón](https://data.geology.gov.yk.ca/) y el [Gobierno de Canadá](https://www.canada.ca/en.html).

La información está organizada de la siguiente forma: 

* **00_Training:** corresponde a un muestreo de datos extraído de once mapas predictores que representan: 

* **00_Virtual_Raster:** esta capa contiene once bandas. Cada una corresponde a un factor condicionante geológico extraído de X1-X11. Para descargarlo acceda al siguiente enlace [Virtual Raster](https://correouisedu-my.sharepoint.com/:i:/g/personal/ana_mantilla_correo_uis_edu_co/EQNRrVHkVXtDqWGktZdeTk0BOgVY7-NYjZdA5DpUPWw9yw?e=9s1VBm)

* **01_Training:** datos de entrenamiento transformados con PCA sin las variables X1 y X2. Contiene nueve componentes principales. Con estos datos se entrenaron los modelos computacionales. 

* **01_Virtual_Raster:** esta capa contiene nueve bandas. Cada una corresponde a un componente principal extraído de las variables X3-X11. Con este archivo se realiza la predicción del mapa de probabilidad. Para descargarlo acceda al siguiente enlace [Virtual Raster con PCA](https://correouisedu-my.sharepoint.com/:i:/g/personal/ana_mantilla_correo_uis_edu_co/EUA5rItvv6JHogINDYS0gJEB8kBQ3PA75Wjof47Sn_6rhQ?e=wO0LDs)

* **Validation:** datos de validación, en total son 20 seleccionados aleatoriamente del conjunto de entrenamiento.

### Pre-requisitos 📋

_Para ejecutar los códigos en el lenguaje de programación Python se requiere un Entorno de Desarrollo Integrado (IDE). En este caso se usó la plataforma Google Collaboratory (https://colab.research.google.com/)_

### Resumen

**1. Análisis preliminar de las variables explicatorias** 📖

* Gráficos de dispersión: se analizaron las matrices de dispersión entre X1-X11. Para abrirlo acceda al archivo '01_dispersion' o de click en el siguiente ícono: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ODoKkmPzCfMmDJR9MxsphMwLP6T4iyqg#scrollTo=Uk3LzYphjYWX)

* Matrices de correlación: se calculó la matriz con el coeficiente de correlación de Pearson. Para abrirlo acceda al archivo '02_correlacion' o de click en el siguiente ícono: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1J-i5zozBfhTm6Xn2MeTuwR4E6xW_btVG)

**2. Remoción de la multicolinealidad: Análisis de componentes principales (PCA)** 📖

* PCA: dado que el análisis de correlación indicó multicolinealidad entre las variables de entrada, se hizo una transformación a los datos con la técnica de análisis de componentes principales. Estos serán los nuevos insumos para el entrenamiento de los modelos y el cálculo de la probabilidad. Para abrirlo acceda al archivo '03_pca' o de click en el siguiente ícono: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qn98JY7233pawnWfeve0OufgNx-jsjfD#scrollTo=pt-SCkOw2qP6)

**3. Técnicas de Aprendizaje Automático** 📖

La predicción de depósitos minerales consiste en un problema de clasificación binaria, en el cual los datos tienen una etiqueta de 1 (depósito) y 0 (no-depósito). 
Para separar las clases se genera un límite de decisión que, según el número de dimensiones, puede ser un plano o hiperplano. Por excelencia los algoritmos usados para resolver tareas de clasificación son: 

* Redes neuronales artificiales: para abrirlo acceda al archivo '04_ann' o de click en el siguiente ícono:[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1RPVJYsLbxpMuZdCMuwng8fdKhc5BvfVX)

* Bosques aleatorios: para abrirlo acceda al archivo '05_rf' o de click en el siguiente ícono:[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1NVgu8JpfByEX-w4MUNyjwoWlWmtNP8Bk)

* Máquinas de soporte vectorial: para abrirlo acceda al archivo '06_svm' o de click en el siguiente ícono: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1sdXfM56fj4yaRhbNbF8qRo6O_2O3t0M4)

## ¿Cómo colaborar con el proyecto ? 

Ayúdame difundiendo. Encuentra errores y repórtalos en un issue en GitHub. También puedes contactarme por medio de mis redes sociales.


## Créditos ✒️

* **Ana Gabriela Mantilla:** anagmd2019@gmail.com </br> <a href="https://www.linkedin.com/in/ana-gabriela-mantilla-24377a21a/">
  <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="HTML tutorial" style="width:30px;height:30px;">
</a> </br> 
* **Paul Goyes:**   goyes.yesid@gmail.com </br> <a href="https://www.linkedin.com/in/paul-goyes-0212b810/">
  <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="HTML tutorial" style="width:30px;height:30px;">
</a>

## Cómo citar ✒️

* Mantilla, A. (2023). Predicción de la ocurrencia de depósitos tipo pórfido usando técnicas de aprendizaje automático [Tesis de pregrado inédita]. Universidad Industrial de Santander.

*Este código se encuentra protegido bajo una licencia de libre acceso. Se permite su distribución y/o modificación, siempre y cuando se consideren los créditos correspondientes. Los autores no se hacen responsables del uso de los códigos por parte de terceros.*



