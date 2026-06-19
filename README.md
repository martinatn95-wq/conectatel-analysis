# 📊 Análisis de Comportamiento de Usuarios (EDA)

## 🎯 Objetivo del proyecto

El objetivo de este proyecto es analizar el comportamiento de usuarios a partir de un dataset de eventos, identificando patrones de interacción, engagement y posibles problemas en la calidad de los datos.

Se busca:

* Entender la frecuencia de uso por usuario
* Analizar la duración de eventos y nivel de interacción
* Detectar inconsistencias en los datos
* Generar insights útiles para la toma de decisiones

---

## 📁 Datasets utilizados

El análisis se basa en datasets simulados de actividad de usuarios, que incluyen las siguientes variables principales:

* `id`: Identificador único de cada evento
* `user_id`: Identificador del usuario
* `duration`: Duración del evento
* `length`: Longitud de la interacción (por ejemplo, texto)
* `city`: Ciudad del usuario
* `plan`: Tipo de plan (Básico / Premium)
* `usage_type`: Tipo de uso (call / text)

---

## 🔍 Etapas del análisis

### 1. Exploración inicial (EDA)

* Revisión de estadísticas descriptivas (`describe`)
* Identificación de valores atípicos y distribuciones
* Detección de valores faltantes

### 2. Limpieza de datos

* Reemplazo de valores inválidos (`-999`, `0`)
* Tratamiento de valores nulos
* Estandarización de variables categóricas (ej. city con valores como `?`)

### 3. Detección y tratamiento de outliers

* Uso del método IQR (rango intercuartílico)
* Eliminación o limitación (capping) de valores extremos

### 4. Feature Engineering

* Creación de métricas por usuario:

  * Número de eventos
  * Duración promedio
  * Longitud promedio de interacción

### 5. Análisis de comportamiento

* Segmentación de usuarios
* Relación entre duración y tipo de uso
* Comparación por tipo de plan

---

##  Cómo ejecutar el notebook

Puedes ejecutar este análisis de las siguientes formas:

### Opción : Local (Jupyter Notebook)

1. Clona este repositorio:

```
git clone https://github.com/tu-usuario/tu-repo.git
```


---

## 🚀 Resultados clave

* Identificación de datos inconsistentes (valores 0 y -999)
* Presencia de outliers significativos en duración y longitud
* Diferencias en comportamiento según tipo de usuario
* Dataset estructurado a nivel evento, permitiendo análisis de engagement

---

## 🧠 Habilidades demostradas

* Limpieza y preprocesamiento de datos
* Análisis exploratorio (EDA)
* Detección de outliers
* Feature engineering
* Análisis de comportamiento de usuarios

---

## 📌 Notas

Este proyecto forma parte de un portafolio enfocado en análisis de datos y está diseñado para simular un caso real de negocio.

---
