# Uso de resumenes para la clasificacion de documentos

**Proyecto del curso Tópicos Selectos de Cómputo**

La clasificación de documentos se hace sobre el conjunto de datos *Amazon Reviews* el cual contiene opiniones de distintos productos y su respectica ponderación basada en número de estrellas, donde entre más estrellas indica un mayor **sentimiento positivo **.
Se transformó a un problema binario donde:
* Contar con 2 o menos estrellas es una reseña negativa
* Contar con 3 o más estrellas se considera una reseña positiva

## Versiones de las reseñas
Se consideraron dos versiones de las reseñas:
* La reseña con un procesamiento que remueve toda la puntuación y convierte el texto a minúsculas.
* La reseña resumida a través de un modelo BERT: Este proceso es bastante tardado por lo que se utilizó PySpark para acelerarlo (De 24 hrs se redujo hasta 4 hrs)

## Técnicas de representación
Se utilizaron dos tipos de técnicas para el proyectoÑ

* **Bag of Words** con 100,200 y 500 tokens
* **FastText** con dimensiones 100 y 200

##Clasificación
Como estrategias de clasificación se estudiaron las siguientes técnicas:

* **Optimización Bayesiana** con dimensiones de Estandarización, Selección de Características, Algoritmos (SVC, KNN, DT y RF) con sus respectivos parámetros
* **Búsqueda Aleatoria Paralelizada en PySpark** con dimensiones de Estandarización, Selección de Características, Algoritmos (SVC, KNN, DT y RF) con sus respectivos parámetros
* **AutoSklearn**
* **AutoPytorch**
