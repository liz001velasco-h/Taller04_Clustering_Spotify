# Taller 04 - Reducción de Dimensionalidad y Clustering con Spotify

## Descripción del Proyecto

Este proyecto desarrolla un flujo completo de aprendizaje no supervisado aplicado a canciones de Spotify, utilizando técnicas de reducción de dimensionalidad y clustering para identificar grupos de canciones similares basándose únicamente en sus características auditivas.

El objetivo principal es simular un caso real de ciencia de datos dentro de una plataforma de streaming musical, donde se busca mejorar sistemas de recomendación sin utilizar etiquetas explícitas como género o artista.

---

# Objetivos

* Realizar limpieza y preparación de datos.
* Aplicar estandarización de variables.
* Reducir dimensionalidad mediante PCA.
* Implementar algoritmos de clustering:

  * K-Means
  * DBSCAN
* Interpretar clusters desde una perspectiva técnica y de negocio.
* Analizar posibles aplicaciones comerciales en plataformas de streaming.

---

#  Dataset

Dataset utilizado:

Spotify Songs and Artists Dataset: https://www.kaggle.com/datasets/glowstudygram/spotify-songs-and-artists-dataset (Kaggle)

Contiene información sobre canciones populares y sus características de audio.

Variables utilizadas:

* track_popularity
* danceability
* energy
* key
* loudness
* mode
* speechiness
* acousticness
* instrumentalness
* liveness
* valence
* tempo

No se utilizaron variables como:

* artista,
* género,
* nombre de canción,
* álbum,

con el fin de evitar sesgos en la agrupación.

---

# Metodología Implementada

El proyecto sigue un pipeline completo de ciencia de datos:

## 1. Limpieza de datos

* Eliminación de valores nulos
* Eliminación de duplicados
* Verificación de tipos de datos

## 2. Análisis exploratorio

* Estadísticas descriptivas
* Histogramas
* Matriz de correlación

## 3. Estandarización

Se utilizó StandardScaler para normalizar las variables debido a sus diferentes escalas.

## 4. Reducción de dimensionalidad

Se aplicó PCA (Principal Component Analysis) para reducir las dimensiones y facilitar la visualización de patrones.

## 5. Clustering

Se implementaron:

* K-Means
* DBSCAN

La selección del número de clusters se realizó utilizando:

* Método del codo
* Silhouette Score

## 6. Interpretación de resultados

Se analizaron los perfiles promedio de cada cluster para identificar características musicales diferenciadoras.

---

# Principales Resultados

* Se identificaron grupos de canciones con patrones auditivos claramente diferenciados.
* Variables como:

  * energy,
  * loudness,
  * valence,
  * tempo
    fueron determinantes en la segmentación.
* K-Means generó clusters más interpretables para el contexto musical.
* PCA permitió representar la información en un espacio bidimensional conservando gran parte de la variabilidad.

---

# Aplicaciones de Negocio

Los resultados obtenidos podrían utilizarse en:

* Sistemas de recomendación musical
* Generación automática de playlists
* Segmentación de usuarios
* Curación de contenido
* Descubrimiento musical personalizado

---

# Tecnologías Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

# Conceptos Aplicados

* Aprendizaje no supervisado
* Reducción de dimensionalidad
* PCA
* Clustering
* K-Means
* DBSCAN
* Estandarización
* Visualización de datos

---

#  Autor

Lizbeth Velasco Hernández

---

# Conclusión General

Este proyecto demuestra cómo las técnicas de aprendizaje no supervisado permiten descubrir patrones relevantes dentro de datos musicales sin necesidad de etiquetas previas. La combinación de PCA y clustering permitió identificar grupos musicales interpretables y potencialmente útiles para sistemas inteligentes de recomendación en plataformas de streaming.
