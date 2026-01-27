# Actividad ML II – Tarea 4  
**Redes Neuronales Artificiales (MLP y CNN) para predicción de Churn**

Este directorio contiene el desarrollo completo de la **Actividad 4** del curso **Machine Learning II**.  
En esta tarea se introduce el uso de **Redes Neuronales Artificiales**, aplicadas al problema de predicción de fuga de clientes (*churn*), utilizando el mismo dataset y preprocesamiento trabajados en las actividades anteriores.

El objetivo principal es comprender el proceso de diseño, entrenamiento y evaluación de redes neuronales, así como analizar sus ventajas y limitaciones frente a modelos clásicos.

---

## Contenido del directorio

### `Actividad 4.pdf`
Documento oficial de la actividad.  
Incluye el contexto, los objetivos de aprendizaje, las instrucciones detalladas y los criterios de evaluación definidos por el curso.

---

### `Actividad4_churn_MLP_CNN_adapted.ipynb`
Notebook base entregado para el desarrollo de la actividad.  
Contiene la estructura inicial y celdas de apoyo que sirven como punto de partida para la implementación de los modelos solicitados.

---

### `Actividad_4.ipynb`
Notebook final de la actividad (**archivo principal de entrega**).  
Incluye el desarrollo completo solicitado en la pauta, abarcando:

- Implementación de una **Red Neuronal Densa (MLP)** para clasificación de churn.
- Justificación de la arquitectura, funciones de activación, función de pérdida y optimizador.
- Análisis del proceso de entrenamiento variando:
  - *Learning rate*.
  - *Batch size*.
- Registro y análisis de la evolución de la función de pérdida y métricas de desempeño.
- Implementación de una **Red Neuronal Convolucional (CNN)** aplicada a una representación matricial simple del dataset.
- Discusión del rol de kernels, stride y pooling en la CNN.
- Evaluación con métricas adecuadas para clases desbalanceadas:
  - Accuracy, Precision, Recall y F1.
  - Curva ROC y AUC-ROC.
  - Curva Precision–Recall y PR-AUC.
- Comparación final entre:
  - Regresión Logística.
  - Random Forest.
  - SVM.
  - Red neuronal artificial (MLP).
  - Red neuronal convolucional (CNN).
- Análisis crítico desde una perspectiva técnica y de negocio.

---

### `data-churn.csv`
Dataset utilizado en la actividad.  
Contiene información de clientes de una empresa de telecomunicaciones, incluyendo variables numéricas y categóricas, junto con la variable objetivo `Churn`, que indica si el cliente abandonó o no el servicio.

---

## Notas metodológicas

- Se mantiene **exactamente el mismo esquema de preprocesamiento** utilizado en las actividades anteriores (imputación de valores faltantes, codificación one-hot y escalamiento de variables numéricas).
- Dado el desbalance de clases presente en el problema de churn, se priorizan métricas como **F1** y **PR-AUC**, por sobre la accuracy.
- Los comentarios dentro del notebook están redactados en **formato de párrafo**, con un lenguaje formal, claro y explicativo, orientado a facilitar la comprensión conceptual del proceso.

