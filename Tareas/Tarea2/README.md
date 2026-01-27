# Actividad ML II – Tarea 2  
**Modelos no lineales para predicción de Churn**

Este directorio contiene el desarrollo completo de la **Actividad 2** del curso **Machine Learning II**, en la cual se extiende el análisis del problema de churn hacia **modelos no lineales basados en árboles**, utilizando Árboles de Decisión y Random Forest.

La actividad se construye sobre el mismo dataset y preprocesamiento utilizados en la Actividad 1, permitiendo una comparación coherente entre modelos lineales y no lineales.

---

## Contenido del directorio

### `Actividad 2.pdf`
Documento oficial de la actividad.  
Incluye el contexto, objetivos de aprendizaje, instrucciones paso a paso y criterios de evaluación definidos por el curso.

---

### `code.ipynb`
Notebook base entregado como punto de partida para el desarrollo de la actividad.  
Contiene la estructura inicial del código, funciones auxiliares y definiciones generales que fueron completadas y extendidas en la solución final.

---

### `Actividad_2_Resuelta.ipynb`
Notebook final de la actividad (**archivo principal de entrega**).  
Incluye el desarrollo completo solicitado en la pauta, abarcando:

- Implementación de un **Árbol de Decisión** para clasificación de churn.
- Selección de hiperparámetros mediante:
  - **Grid Search Cross-Validation**
  - **Randomized Search Cross-Validation**
- Comparación de desempeño predictivo y **tiempos de ejecución** entre ambos métodos de búsqueda.
- Visualización e interpretación del **árbol óptimo**.
- Implementación de **Random Forest** con validación cruzada estratificada.
- Análisis explícito de la **varianza de las predicciones** al variar el número de árboles.
- Gráficos de:
  - Varianza vs número de árboles.
  - Métricas de clasificación vs número de árboles.
- Selección del mejor Random Forest mediante búsqueda de hiperparámetros.
- Comparación final entre:
  - Árbol de Decisión
  - Random Forest
- Evaluación con métricas robustas para problemas desbalanceados:
  - Accuracy, Precision, Recall, F1
  - Curva ROC y AUC-ROC
  - Curva Precision–Recall y PR-AUC
- Análisis crítico y conclusiones desde una perspectiva técnica y de negocio.

---

### `data-churn.csv`
Dataset utilizado en la actividad.  
Contiene información de clientes de una empresa de telecomunicaciones, incluyendo variables numéricas y categóricas, junto con la variable objetivo `Churn`, que indica si el cliente abandonó o no el servicio.

---

## Notas

- Se mantiene **exactamente el mismo preprocesamiento** definido en la Actividad 1 (imputación, codificación y escalamiento) para asegurar consistencia y comparabilidad entre modelos.
- Dado el desbalance de clases en el problema de churn, se prioriza el uso de métricas como **F1** y **PR-AUC**, por sobre la accuracy.
- Se analiza explícitamente la relación entre **ensambles, reducción de varianza y generalización**, en concordancia con la teoría vista en clases.
