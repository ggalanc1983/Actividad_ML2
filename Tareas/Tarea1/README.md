# Actividad ML II – Tarea 1  
**Predicción de Churn con Regresión Logística**

Este directorio contiene los archivos correspondientes a la **Actividad 1** del curso **Machine Learning II**, cuyo objetivo es predecir la probabilidad de fuga de clientes (*churn*) en una empresa de telecomunicaciones, utilizando modelos de **Regresión Logística** y distintas estrategias de preprocesamiento y regularización.

---

## Contenido del directorio

### `Actividad 1.pdf`
Documento oficial de la actividad, que contiene el enunciado, los objetivos, las instrucciones y los criterios de evaluación definidos por el curso.

---

### `Codigo original.ipynb`
Notebook base utilizado como punto de partida para el desarrollo de la actividad.  
Incluye la estructura inicial del código y las primeras aproximaciones al problema, sobre las cuales se construyó la solución final.

---

### `Actividad_1_Resuelta.ipynb`
Notebook final de la actividad.  
Contiene el desarrollo completo solicitado en la pauta, incluyendo:

- Carga y exploración del dataset.
- Preprocesamiento de datos (imputación, codificación y escalamiento).
- Entrenamiento de modelos de Regresión Logística:
  - Modelo base.
  - Modelo con transformaciones polinomiales (grado 2).
  - Modelos regularizados (L2 y Elastic Net).
- Evaluación mediante validación cruzada estratificada (k-fold).
- Métricas de desempeño: accuracy, precision, recall, F1, ROC-AUC y PR-AUC.
- Curvas ROC y Precision–Recall promedio.
- Análisis crítico y conclusiones alineadas con la pauta de la actividad.

Este notebook corresponde al **archivo principal de entrega**.

---

### `data-churn.csv`
Dataset utilizado para el desarrollo de la actividad.  
Contiene información de clientes de una empresa de telecomunicaciones, incluyendo variables numéricas y categóricas, junto con la variable objetivo `Churn`, que indica si el cliente abandonó o no el servicio.

---

## Notas adicionales

- El enfoque prioriza métricas adecuadas para problemas con **desbalance de clases**, especialmente **F1** y **PR-AUC**, por sobre la accuracy.
- La estructura del notebook y los textos explicativos están diseñados para facilitar la comprensión del proceso completo de modelamiento y evaluación.
- El contenido de este directorio está pensado para ser revisado tanto a nivel técnico como conceptual.
