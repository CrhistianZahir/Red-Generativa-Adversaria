<h2 align="center">Red Generativa Adversaria</h2>

<h2 align="center">🔧Áreas de conocimiento empleadas</h2>
<p align="center">
Aprendizaje no supervisado - Visión por computador - Inteligencia artificial - Redes Neuronales
</p>
<h2 align="center">🔧 Frameworks</h2>

<p align="center">
  <img src="https://img.shields.io/badge/Tensorflow-FF6F00?style=for-the-badge&logo=Tensorflow&logoColor=white" />
  <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=Keras&logoColor=white" />
</p>

<h2 align="center">Introducción</h2>
<p align="center">
En este proyecto se desarrolla una red generativa adversativa, esta es un algoritmo de inteligencia artificial empleado en el área de aprendizaje no supervisado compuesta por un sistema de dos redes neuronales, una red generadora mientras que, una red discriminadora evalúa por medio de la capacidad de discernir entre los datos reales y los generados. El presente trabajo tiene como objetivo principal implementar una red generativa adversativa y entrenarla para que obtenga la capacidad de generar imágenes de aves. En el presente documento encontrará información sobre la etapa de diseño, implementación, resultados y conclusiones obtenidas del desarrollo de la actividad.

Objetivos:


*   Seleccionar el dataseet y el conjunto de imágenes a tratar para la construcción de la red generativa adversativa.
*   Definir la red generadora y la red discriminadora.
*   Establecer los parámetros de optimización, función de pérdida, el learning rate y el batch size.
</p>
<h2 align="center">Diseño</h2>
<p align="center">
En el presente documento se desarrollo una red generativa adversativa, A continuación, se describe las principales características que se tuvieron en cuenta para su diseño:
Se utilizó el conjunto de datos CIFAR-10, compuesto por 60000 imágenes, divididas en 50000 imágenes para el proceso de entrenamiento y 10000 para el proceso de prueba. Una característica relevante de este conjunto de datos es que contiene 10 clases (aviones, automóviles, aves, gatos, ciervos, perros, ranas, caballos, barcos y camiones). Las imágenes tienen un tamaño de 32 píxeles de ancho y 32 píxeles de alto, en este caso, se utilizará únicamente la clase denominada como aves (birds).

Descripción de la arquitectura de la red.

Para que la red tenga la capacidad de generar imágenes, se utilizarán las siguientes dos redes neuronales:

•	Red generadora: Esta red neuronal en un principio generará ruido, pero con el debido entrenamiento obtendrá la capacidad de generar imágenes, está compuesta por:

Capa de entrada (Densa), ruido con una dimensión igual a 100 y una función de activación “LeakyReLU”.

Capa de configuración (Reshape), toma la salida de la capa Densa.

Capas de convolución transpuesta, se utilizarán tres de estas capas para aumentar las dimensiones de la imagen, se utiliza un kernel 3x3 y un stride de 2. Seguido de cada una de estas capas se utiliza una función de activación “LeakyReLU”.

Capa de salida, esta última capa convolucional tiene una salida de 3 canales (RGB) y utiliza una función de activación tangente hiperbólica.

•	Red discriminadora: Esta red determina si una imagen es real o no y servirá para entrenar la red generadora, está compuesta por:

Cuatro capas ocultas seguidas por funciones de activación “LeakyReLU”.

Una capa de “aplanamiento” Flatten.

Una capa de Dropout.

Por último, una capa Densa como salida de esta red neuronal convolucional.

En cuanto a frameworks se utilizó Tensorflow y Keras, además se utilizó una herramienta nueva que en clases anteriores no se había usado como lo es la herramienta Conv2DTranspose, la cual básicamente se usa en la red generadora para agrandar la imagen a medida que se convoluciona.
</p>
<h2 align="center">Conclusiones</h2>
<p align="center">
El desarrollo de la red generativa adversativa permitió manipular una herramienta nueva, esta herramienta o librería se llama Conv2DTranspose, la cual básicamente se usa en la red generadora para agrandar la imagen a medida que se convoluciona.

El desarrollo del presente trabajo permitió comprender de mejor forma la composición de una red generativa adversativa, la cual basicamente se compone de una red generadora y una red discriminadora, en la que se observó que la arquitectura y composición de la discriminadora es una red neuronal convolucional que utiliza "Conv2D" para su construcción, mientras que, la red generadora utiliza "Conv2DTranspose" para la construcción de sus capas.

Tras la realización de la actividad y de llevar a cabo diversas pruebas se estableció como parámetro optimizador Adam, la función de pérdida "binary_crossentropy", un valor de learning rate igual a 0.0002 y un valor de batch size igual a 128 y un número total de épocas igual a 350.

La aplicabilidad de este tipo de red en el ámbito del desempeño profesional en mi caso como ingeniero electrónico, se presenta como una herramienta de la inteligencia artificial para abordar problemáticas donde es difícil obtener datos reales o son insuficientes, siendo una solución para entrenar modelos de aprendizaje automático en aplicaciones como lo pueden ser los sistemas de detección de objetos y reconocimiento de señales.
</p>
<h2 align="center">Referencias</h2>
<p align="center">
1.   CIFAR-10 and CIFAR-100 datasets. (s/f). Toronto.edu. Recuperado el 10 de marzo de 2024, de https://www.cs.toronto.edu/~kriz/cifar.html

2.   Jauregui, A. F. (2020, julio 13). Cómo crear una Red Generativa Antagónica (GAN) en Python. Ander Fernández; Ander Fernández Jauregui. https://anderfernandez.com/blog/como-crear-una-red-generativa-antagonica-gan-en-python/

3.   Wikipedia contributors. (s/f). Red generativa adversativa. Wikipedia, The Free Encyclopedia. https://es.wikipedia.org/w/index.php?title=Red_generativa_adversativa&oldid=152476624
</p>
