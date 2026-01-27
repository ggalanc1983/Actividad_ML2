# Actividad ML II – Tarea 3  
**Naïve Bayes y Support Vector Machines para predicción de Churn**

Este directorio contiene el desarrollo completo de la **Actividad 3** del curso **Machine Learning II**.  
El objetivo de esta actividad es analizar y comparar el desempeño de **modelos probabilísticos y de margen** aplicados al problema de predicción de fuga de clientes (*churn*) en una empresa de telecomunicaciones.

La actividad continúa el trabajo realizado en las tareas anteriores, utilizando el **mismo dataset** y el **mismo flujo de preprocesamiento**, con el fin de asegurar comparabilidad entre los distintos enfoques de modelamiento.

---

## Contenido del directorio

### `Actividad 3.pdf`
Documento oficial de la actividad.  
Incluye el enunciado, los objetivos de aprendizaje, las instrucciones específicas y los criterios de evaluación definidos por el curso.

---

### `code.ipynb`
Notebook base entregado como punto de partida para el desarrollo de la actividad.  
Contiene la estructura inicial y funciones auxiliares que se mantienen sin modificaciones y sobre las cuales se construye la solución final.

---

### `Actividad_3.ipynb`
Notebook final de la actividad (**archivo principal de entrega**).  
Incluye el desarrollo completo solicitado en la pauta, abarcando:

- Implementación de **Naïve Bayes (GaussianNB)** para clasificación de churn.
- Selección de hiperparámetros mediante **Grid Search**.
- Evaluación con conjunto de test y validación cruzada estratificada.
- Análisis del supuesto de **independencia condicional** y su impacto en el desempeño.
- Implementación de **Support Vector Machines (SVM)**:
  - SVM lineal.
  - SVM con kernel RBF.
- Comparación entre **Grid Search** y **Randomized Search**, considerando desempeño y tiempo computacional.
- Evaluación con métricas adecuadas para clases desbalanceadas:
  - Accuracy, Precision, Recall y F1.
  - Curva ROC y AUC-ROC.
  - Curva Precision–Recall y PR-AUC.
- Uso de `class_weight='balanced'` para analizar el impacto del desbalance de clases.
- Análisis crítico comparando Naïve Bayes, SVM lineal y SVM RBF desde una perspectiva técnica y de negocio.

---

### `data-churn.csv`
Dataset utilizado en la actividad.  
Contiene información de clientes de una empresa de telecomunicaciones, incluyendo variables numéricas y categóricas, junto con la variable objetivo `Churn`, que indica si el cliente abandonó o no el servicio.

---

## Notas

- Se mantiene **exactamente el mismo preprocesamiento** utilizado en las Actividades 1 y 2 (imputación de valores faltantes, codificación one-hot y escalamiento de variables numéricas).
- Dado el desbalance de clases presente en el problema de churn, se priorizan métricas como **F1** y **PR-AUC**, por sobre la accuracy.
- Los comentarios dentro del notebook están redactados en **formato de párrafo**, con un lenguaje formal y explicativo, orientado a facilitar la comprensión conceptual del proceso.

