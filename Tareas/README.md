# Machine Learning II – Proyecto Churn  
**Repositorio de tareas y actividades**

Este repositorio contiene el desarrollo completo de las actividades del curso **Machine Learning II**, todas ellas basadas en el problema de **predicción de fuga de clientes (churn)** en una empresa de telecomunicaciones.

A lo largo de las distintas tareas se exploran y comparan **modelos clásicos y modelos avanzados**, manteniendo de forma consistente el mismo dataset y un esquema base de preprocesamiento, lo que permite analizar de manera progresiva las ventajas, limitaciones y costos de cada enfoque.

---

##  Estructura del repositorio

### `Tarea1`
Modelos lineales para clasificación de churn.
- Regresión Logística.
- Validación cruzada estratificada.
- Métricas para clases desbalanceadas (F1, PR-AUC).
- Análisis crítico orientado a negocio.

---

### `Tarea2`
Modelos basados en árboles.
- Árbol de Decisión con búsqueda de hiperparámetros.
- Random Forest y análisis de reducción de varianza.
- Comparación de desempeño y costo computacional.
- Interpretabilidad y estabilidad de modelos.

---

### `Tarea3`
Modelos probabilísticos y de margen.
- Naïve Bayes.
- Support Vector Machines (SVM lineal y RBF).
- Comparación de Grid Search y Random Search.
- Análisis del rol del escalamiento y la dimensionalidad.
- Evaluación desde una perspectiva técnica y de negocio.

---

### `Tarea4`
Redes neuronales.
- Red neuronal densa (MLP).
- Análisis de learning rate y batch size.
- Red neuronal convolucional (CNN) aplicada a datos tabulares.
- Comparación con modelos tradicionales.
- Discusión sobre desempeño, interpretabilidad y escalabilidad.

---

## Enfoque metodológico común

Todas las tareas comparten los siguientes criterios metodológicos:

- Uso del **mismo dataset de churn**.
- Esquema base de **preprocesamiento consistente**:
  - Imputación de valores faltantes.
  - Codificación one-hot de variables categóricas.
  - Escalamiento de variables numéricas.
- Evaluación con métricas adecuadas para problemas desbalanceados, priorizando **F1** y **PR-AUC**.
- Notebooks con código ordenado y comentarios explicativos en formato de párrafo.

---

## Objetivo académico

El objetivo del repositorio es **comprender de manera comparativa** cómo distintos modelos de aprendizaje automático abordan un mismo problema real, evaluando no solo el desempeño predictivo, sino también aspectos como interpretabilidad, estabilidad, costo computacional y utilidad práctica desde una perspectiva de negocio.

