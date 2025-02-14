# Project05-NLP_ANALISIS_SENTIMIENTOS

# 📊 **Informe Final: Análisis de Sentimiento en Reviews de Videojuegos**

## 📌 **1. Introducción**

En este proyecto se ha desarrollado un modelo de **análisis de sentimiento** aplicado a reseñas de videojuegos. El objetivo era clasificar las reseñas en **positivas** o **negativas**, utilizando técnicas de procesamiento de lenguaje natural (NLP) y modelos de machine learning.

## 📌 **2. Preprocesamiento de Datos**

- Se ha utilizado un dataset de reseñas de videojuegos, eliminando valores nulos y realizando limpieza de texto.
- Se ha aplicado **tokenización optimizada con GPU** mediante `spaCy`.
- Para la vectorización del texto, se ha combinado **TF-IDF** con **Word2Vec**, con el objetivo de capturar tanto la frecuencia como la semántica de las palabras.
- Se ha utilizado **SMOTE** para balancear las clases y evitar problemas de desbalanceo en los datos de entrenamiento.

## 📌 **3. Modelos Entrenados y Comparación**

Se han probado los siguientes modelos:

- **Regresión Logística**
- **Random Forest**
- **XGBoost** (con aceleración en GPU)
- **LightGBM** (con aceleración en GPU)

Para la selección del mejor modelo, se evaluaron las siguientes métricas:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- **Curva ROC y AUC**

## 📌 **4. Resultados**

Los modelos presentaron los siguientes desempeños:

| Modelo              | Accuracy | Precision | Recall | F1-score | AUC  |
| ------------------- | -------- | --------- | ------ | -------- | ---- |
| Regresión Logística | 0.79     | 0.80      | 0.96   | 0.87     | 0.77 |
| Random Forest       | 0.83     | 0.86      | 0.93   | 0.89     | 0.84 |
| XGBoost             | 0.79     | 0.86      | 0.87   | 0.87     | 0.79 |
| LightGBM            | 0.80     | 0.87      | 0.88   | 0.87     | 0.81 |

El **mejor modelo según las métricas** fue **Random Forest**, seguido de **LightGBM**, ambos con una buena combinación de **precisión** y **recall**.

## 📌 **5. Visualizaciones Clave**

Se han generado diversas visualizaciones para el análisis del modelo:

- **Matriz de Confusión**: Para evaluar los errores de clasificación.
- **Curva ROC y AUC**: Para comparar la capacidad predictiva de los modelos.
- **Distribución de Probabilidades de Predicción**: Para analizar la confianza de las predicciones.

## 📌 **6. Predicciones sobre Nuevas Frases**

Se realizaron pruebas con frases nuevas y el modelo fue capaz de clasificar correctamente reseñas positivas y negativas. Esto valida su capacidad para generalizar a datos no vistos.

## 📌 **7. Conclusiones y Futuras Mejoras**

**Conclusiones:**

- La combinación de **TF-IDF y Word2Vec** ha sido efectiva para capturar la semántica del texto.
- **Random Forest** ha demostrado ser el modelo más robusto en términos de balance entre precisión y recall.
- El balanceo de clases con **SMOTE** ha mejorado significativamente el rendimiento del modelo.

**Posibles Mejoras:**

- Implementar modelos más avanzados como **BERT o Transformers** para mejorar el rendimiento.
- Incluir métricas de interpretabilidad, como la importancia de palabras en los modelos de árboles.
- Ampliar el dataset con más reseñas para mejorar la generalización del modelo.




