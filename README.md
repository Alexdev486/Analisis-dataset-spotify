# 📊 Análisis Exploratorio del Dataset de Spotify (R)

## 📁 Archivo

`AnalisisdatasetR.ipynb`

Notebook en **R** (ejecutado en entorno tipo Google Colab / Jupyter) destinado al **análisis exploratorio de datos (EDA)** y **preparación de features** a partir de un dataset musical de Spotify previamente procesado.

---

## 🎯 Objetivo del notebook

El objetivo principal es:

* Comprender la estructura y calidad del dataset
* Analizar la popularidad musical desde múltiples perspectivas
* Generar **variables derivadas** útiles para análisis avanzado y modelos de Machine Learning
* Visualizar patrones relevantes mediante gráficos estadísticos

Este notebook sirve como **base analítica** para:

* Modelado predictivo
* Dashboards
* Diseño de base de datos
* Backends de análisis musical

---

## 📦 Dataset utilizado

**Archivo de entrada** (esperado):

* `processed_spotify_eda_final.csv`

El dataset contiene información sobre:

* Artistas
* Álbumes
* Canciones
* Fechas de lanzamiento
* Popularidad
* Métricas derivadas (normalizadas, categorizadas y transformadas)

El CSV ya ha pasado por un proceso previo de limpieza y enriquecimiento.

---

## 🧠 Contenido del análisis

### 1️⃣ Carga y exploración inicial

* Lectura del CSV
* Inspección de dimensiones
* Tipos de variables
* Detección de valores nulos

---

### 2️⃣ Limpieza y preprocesado

* Conversión de fechas
* Creación de variables temporales:

  * Año
  * Mes
  * Década
* Normalización y estandarización de métricas

---

### 3️⃣ Feature Engineering

Se generan variables analíticas como:

* Duración en minutos y z-score
* Popularidad estandarizada
* Logaritmo de seguidores del artista
* Posición relativa del track en el álbum
* Número de géneros asociados
* Métricas basadas en el título de la canción

Estas features están pensadas para **modelos de ML y análisis estadístico**.

---

### 4️⃣ Análisis exploratorio (EDA)

Visualizaciones clave:

* Distribución de popularidad
* Boxplots por categoría de popularidad
* Relación entre popularidad y duración
* Análisis temporal por año y década
* Mapas de correlación entre variables numéricas

Se utilizan principalmente:

* `ggplot2`
* `dplyr`
* `tidyr`

---

### 5️⃣ Resultados principales

* La popularidad presenta una distribución sesgada
* Existen diferencias claras entre categorías de popularidad
* Algunas features derivadas muestran alta correlación
* El tiempo de lanzamiento influye en métricas de éxito

Estos resultados justifican la posterior **normalización del dataset y su diseño relacional**.

---

## 🛠️ Requisitos

Entorno R con los siguientes paquetes:

```r
library(tidyverse)
library(ggplot2)
library(dplyr)
library(lubridate)
library(scales)
```

En Google Colab:

```r
install.packages(c("tidyverse", "lubridate", "scales"))
```

---

## ▶️ Ejecución

1. Subir el CSV al entorno (`/content/` en Colab)
2. Abrir `AnalisisdatasetR.ipynb`
3. Ejecutar las celdas en orden

No se requiere configuración adicional.

---

## 📌 Relación con otros componentes del proyecto

Este notebook:

* Alimenta el diseño de la **base de datos relacional**
* Genera las **features usadas en ML**
* Justifica decisiones de modelado
* Sirve como documentación analítica

---

## 🚀 Posibles extensiones

* Incorporar audio features de la API de Spotify
* Añadir análisis por playlists
* Modelos predictivos de popularidad
* Integración con FastAPI

---

## 📄 Licencia

Uso académico y educativo.

---

**Autor**: Alex
**Contexto**: Análisis de datos / Inteligencia Artificial
