# 6. TEXT REPRESENTATION

## - en qué consiste BOW, bag of words, que inconvenientes tiene﻿


El modelo Bag of Words (Bolsa de Palabras, BOW) es un enfoque simplificado utilizado en procesamiento de lenguaje natural y minería de texto para representar documentos de texto o corpus. Consiste en descomponer el texto en palabras y contar la frecuencia de cada palabra, sin considerar el orden o la estructura gramatical de las palabras en el documento.

Inconvenientes del modelo BOW:

- Pérdida de contexto: BOW ignora el orden de las palabras y la estructura de las oraciones, lo que significa que se pierde el contexto y la información semántica.
- Sinónimos y polisemia: No distingue entre palabras con múltiples significados (polisemia) ni reconoce sinónimos, lo que puede llevar a interpretaciones incorrectas del texto.
- Alta dimensionalidad: El tamaño del vector puede ser muy grande si el vocabulario es amplio, lo que aumenta la complejidad computacional.
- Frecuencia vs. Importancia: BOW se basa en la frecuencia de las palabras, lo que no siempre se correlaciona con la importancia de las palabras en el texto. Palabras comunes pueden dominar en la representación sin ser informativas.

## - en qué consisten la técnica de Bag of n-grams, cuales son sus desventajas

La técnica de Bag of n-grams es una extensión del modelo Bag of Words (BOW) que, en lugar de considerar solo palabras individuales (1-grams o unigrams), toma en cuenta la secuencia de n palabras consecutivas (n-grams) para preservar un poco más de contexto y estructura del texto. Un n-gram es una secuencia contigua de n ítems (en este caso, palabras) extraída de un texto o secuencia de habla.

Desventajas del modelo Bag of n-grams:

- Aumento de la dimensionalidad: A medida que n aumenta, la cantidad de posibles n-grams crece exponencialmente, lo que puede llevar a una alta dimensionalidad y, en consecuencia, a un mayor requerimiento de memoria y tiempo de procesamiento.
- Datos dispersos: Muchos n-grams pueden ocurrir pocas veces, resultando en vectores donde la mayoría de los elementos son cero (vectores dispersos), lo cual puede ser ineficiente desde el punto de vista computacional.
- Pérdida de información: Aunque los n-grams capturan más contexto que los unigrams, aún hay pérdida de información, especialmente con respecto a la estructura global del texto y las relaciones a larga distancia entre palabras.
- Sensibilidad al ruido: Los n-grams son sensibles a errores en el texto, como errores tipográficos o gramaticales, que pueden generar n-grams incorrectos o irrelevantes.
- Generalización: Los n-grams que no se han visto durante el entrenamiento no serán reconocidos por el modelo, lo que puede afectar la capacidad del modelo para generalizar bien a nuevos textos.

## - en qué consiste TF-IDF, ¿por qué es es mejor que el método anterior?


TF-IDF, que significa "Frecuencia de Término - Frecuencia Inversa de Documento", es una técnica utilizada en la minería de textos y la recuperación de información para reflejar la importancia de una palabra en un documento en relación con una colección de documentos o corpus. A diferencia del modelo Bag of Words (BOW) o Bag of n-grams, que se basa simplemente en la frecuencia de las palabras, TF-IDF proporciona una ponderación más informativa de las palabras.

¿Por qué es TF-IDF mejor que los métodos anteriores?

- Relevancia sobre frecuencia: TF-IDF supera una limitación clave del BOW y Bag of n-grams al diferenciar entre palabras comunes y palabras significativas para el documento. Las palabras comunes en todo el corpus reciben una puntuación más baja, mientras que las palabras importantes y únicas para algunos documentos reciben una puntuación más alta.

- Mejora la recuperación y clasificación de información: Al ponderar las palabras por su relevancia, TF-IDF mejora la calidad de las características utilizadas para tareas como la clasificación de textos, la agrupación de documentos y la búsqueda de información, ya que las palabras con altos valores de TF-IDF son más descriptivas y distintivas para los documentos.

- Reducción de ruido: Al dar menos peso a las palabras que aparecen en muchos documentos (como las palabras de parada), TF-IDF ayuda a reducir el ruido y se enfoca en la información más relevante dentro de los documentos.
