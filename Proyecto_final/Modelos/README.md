# Modelos de Aprendizaje Automático – Proyecto ML II

Este directorio contiene los **modelos de aprendizaje automático implementados y evaluados** en el marco del proyecto, orientado a la **predicción de la intensidad de incendios forestales** mediante el valor máximo de **Fire Radiative Power (FRP_max)** y la **detección operativa de eventos intensos (FRP ≥ 100 MW)**.

El enfoque metodológico es **regresión + clasificación derivada**, lo que permite evaluar los modelos tanto desde una perspectiva predictiva continua como desde un punto de vista operativo para sistemas de alerta y priorización de recursos.

---

## Contenido del directorio

### `ML_II_Modelo_1_Ridge.ipynb`
**Modelo baseline – Ridge Regression (lineal)**

- Modelo de regresión lineal regularizada para predecir `frp_max`.
- Clasificación derivada:
  - Evento intenso = 1 si `frp_max_pred ≥ 100`.
- Incluye:
  - Preprocesamiento (imputación + escalado).
  - Optimización del parámetro de regularización mediante GridSearchCV.
  - Métricas de regresión (MAE, RMSE, R²).
  - Métricas de clasificación (Precision, Recall, F1).
  - Matriz de confusión con rotulación explícita (TN, FP, FN, TP).
- Rol: **modelo base de referencia lineal**.

---

### `ML_II_Modelo_Ridge_con_Clasificación_Polinomial.ipynb`
**Ridge Regression con transformación polinomial (baseline no lineal)**

- Extensión del modelo Ridge mediante **características polinomiales de grado 2**.
- Permite capturar:
  - Relaciones no lineales suaves.
  - Interacciones simples entre variables climáticas.
- Mantiene regularización explícita para controlar la complejidad.
- Misma lógica de clasificación operativa (FRP ≥ 100).
- Rol: **baseline intermedio** entre Ridge lineal y modelos no paramétricos.

---

### `ML_II_Random_Forest.ipynb`
**Modelo no lineal basado en árboles – Random Forest**

- Modelo de referencia principal del proyecto.
- Capaz de capturar:
  - No linealidades complejas.
  - Interacciones múltiples.
  - Comportamiento en colas altas del FRP.
- Incluye:
  - Optimización de hiperparámetros.
  - Evaluación completa en regresión y clasificación derivada.
- Rol: **mejor desempeño global**, especialmente en detección de eventos intensos.

---

### `ML_II_Redes_Neuronales.ipynb`
**Red neuronal multicapa (MLP)**

- Modelo de red neuronal para regresión de `frp_max`.
- Incluye:
  - Preprocesamiento obligatorio (escalado).
  - Regularización (Dropout, Early Stopping).
  - Variante mejorada con transformación logarítmica y pérdida Huber.
- Clasificación derivada por umbral FRP ≥ 100.
- Rol: **comparación con enfoques neuronales en datos tabulares**.

---

## Criterio operativo común

En todos los modelos se utiliza el mismo criterio de clasificación derivada:

> **Evento intenso = 1 ⇔ FRP_max_predicho ≥ 100 MW**

Este criterio permite evaluar los modelos desde una perspectiva **operativa y aplicada**, más allá de métricas puramente regresivas.

---

## Estructura metodológica

1. Predicción continua de `frp_max`.
2. Transformación a clasificación binaria mediante umbral fijo.
3. Evaluación con métricas adecuadas al desbalance de clases.
4. Comparación progresiva:
   - Ridge lineal → Ridge polinomial → Random Forest → MLP.

---

## Nota final

Estos notebooks están **documentados y comentados por etapas**, con énfasis en la interpretación de resultados y la justificación metodológica, y están diseñados para su uso en **contextos académicos y de análisis aplicado**.
