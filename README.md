# 📝 NLP Model for Sentiment Analysis

Este repositorio contiene un proyecto de Procesamiento de Lenguaje Natural (NLP) desarrollado como parte de una asignatura. El objetivo fue entrenar un modelo capaz de detectar **reseñas negativas** a partir de un conjunto de opiniones de clientes.

## 📌 Project Overview

- **Objetivo**: Clasificar las reseñas de clientes como negativas o no.
- **Reto**: El conjunto de datos tenía **clases desbalanceadas**, con menos reseñas negativas que positivas.
- **Enfoque**: Comparar el rendimiento de diferentes modelos y técnicas de preprocesamiento ante este desequilibrio.

## ⚙️ Methods and Tools

- Modelos utilizados: `Logistic Regression`, `Random Forest`
- Técnicas aplicadas:
  - Uso del parámetro `class_weight='balanced'` para tratar el desbalanceo
  - Eliminación de palabras vacías estándar (se mantuvieron negaciones como _not_, _no_, _didn't_)
  - Evaluación de los modelos con foco en la detección de **reseñas negativas**

## 📊 Key Conclusions

- ✅ **Manejo del desbalanceo**:  
  Es más efectivo usar la opción `class_weight='balanced'` dentro de los modelos que aplicar técnicas de muestreo manualmente.

- 🧹 **Stop words**:  
  Eliminar palabras vacías personalizadas (como _not_, _no_, _didn't_) **no mejoró** los resultados. Solo se eliminaron las stop words estándar.

- ⚖️ **Rendimiento del modelo**:  
  No existe una solución perfecta. La elección depende del objetivo del problema: minimizar **falsos negativos** o **falsos positivos** según el contexto.

- 🔍 **Regresión logística vs. Random Forest**:  
  Tras entrenar ambos modelos con el dataset completo y desbalanceado utilizando `class_weight='balanced'`:
  - La **Regresión Logística** tuvo mejores resultados en la detección de **reseñas negativas**
  - Esto la convierte en una opción interesante para empresas que quieran identificar opiniones negativas y actuar en consecuencia.

## 🔮 Future Improvements

- 🛠️ Aplicar **GridSearchCV** para optimizar los hiperparámetros del modelo Random Forest.
- 🤖 Explorar enfoques de **Deep Learning**, como **BERT** u otros modelos basados en transformers, para capturar patrones más complejos en el lenguaje.

