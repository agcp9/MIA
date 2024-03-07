# 3.  Stemming y Lemmatization
## - ¿Que son cada una y cuales son sus diferencias?
## y algun ejemplo

Stemming y lemmatization son dos técnicas utilizadas en el procesamiento del lenguaje natural para reducir las palabras a su forma base o raíz, aunque operan de maneras ligeramente diferentes y tienen distintos propósitos y resultados.

Stemming:

- Stemming implica cortar las terminaciones de las palabras para intentar llegar a la raíz o "stem" de la palabra, que no necesariamente tiene que ser una palabra válida en el idioma.
- El proceso de stemming es más simple y rápido que la lemmatization, ya que se basa en reglas heurísticas para cortar las terminaciones de las palabras sin considerar el contexto.
- **Por ejemplo, "running", "runs" y "runner" podrían ser reducidas al stem "run".**
- Los algoritmos de stemming, como el algoritmo de Porter, no necesitan conocimiento del contexto y no garantizan que el resultado sea una palabra válida en el idioma de interés.
- Es útil en situaciones donde la identificación precisa de la forma base de la palabra no es crítica, como en la búsqueda y recuperación de información.

Lemmatization:

- La lemmatization, por otro lado, reduce las palabras a su lema, que es la forma base o canónica de una palabra según su diccionario.
- A diferencia del stemming, la lemmatization considera el contexto y la parte del discurso de la palabra, lo que requiere más conocimiento del idioma y hace que el proceso sea más lento pero más preciso.
-** Por ejemplo, "am", "are" y "is" se reducen al lema "be", y "running" se reduce a "run".**
- La lemmatization es más sofisticada que el stemming y es útil en tareas que requieren un nivel alto de precisión lingüística, como en el análisis de sentimientos o en la traducción automática.

Diferencias clave:

- El stemming puede no resultar en una palabra existente en el idioma, mientras que la lemmatization siempre produce palabras válidas.
- La lemmatization tiene en cuenta el contexto y la categoría gramatical de la palabra, mientras que el stemming opera a nivel de cadena de texto, aplicando reglas fijas sin considerar el contexto.
- La lemmatization es más adecuada para aplicaciones que requieren precisión lingüística, mientras que el stemming es más rápido y puede ser preferible en aplicaciones donde la velocidad es crucial y la precisión lingüística es menos importante.

## - para que reducimos las palabras de un texto


Reducir las palabras de un texto a su forma base o raíz a través de técnicas como stemming y lemmatization es una práctica común en el procesamiento del lenguaje natural (NLP) por varias razones clave:

** Reducir la complejidad:** Al convertir las palabras a su forma base, reducimos la variabilidad del lenguaje, lo que disminuye la complejidad del texto y el tamaño del vocabulario con el que deben trabajar los algoritmos de NLP.

** Mejorar la precisión de la búsqueda: **Cuando se indexan documentos para la búsqueda, reducir las palabras a su forma base permite que una consulta devuelva resultados relevantes incluso si la forma exacta de la palabra no coincide, mejorando la relevancia y la cobertura de la búsqueda.

** Unificar términos similares:** La reducción permite tratar como iguales variantes de una misma palabra (por ejemplo, "correr", "corriendo", "corre"), lo cual es crucial para análisis agregados, como el conteo de frecuencias o la determinación de la relevancia de términos en un corpus.

** Facilitar el análisis semántico:** Al estandarizar las palabras a su lema o raíz, es más fácil analizar y comparar el significado de los textos, ya que se minimizan las variaciones superficiales en la forma de las palabras.

** Optimizar el entrenamiento de modelos: **En el aprendizaje automático, reducir la dimensionalidad de los datos (en este caso, la cantidad de palabras únicas) puede mejorar la eficiencia del entrenamiento y la efectividad de los modelos, ya que los modelos pueden enfocarse en aprender relaciones más generales en lugar de particularidades específicas del uso de palabras.

** Mejorar la consistencia en el procesamiento del lenguaje: **Especialmente en idiomas con rica flexión morfológica, la reducción a la forma base ayuda a mantener la consistencia al procesar variantes de una palabra, lo que es vital para tareas como el análisis de sentimientos, la clasificación de textos o la extracción de información.

En resumen, la reducción de palabras a su forma base en NLP facilita y mejora el análisis del texto, la extracción de información relevante y la eficiencia general de los algoritmos y modelos utilizados en diversas aplicaciones de procesamiento del lenguaje.

