# Proyecto Final – Machine Learning II  
**Predicción de la transición de intensidad en incendios forestales (Región del Biobío, Chile)**

Este repositorio contiene el **Proyecto Final** del curso **Machine Learning II**, cuyo enfoque es el desarrollo y evaluación de un modelo de aprendizaje automático orientado a **anticipar la ocurrencia de incendios forestales de alta intensidad energética** en la Región del Biobío, Chile.

A diferencia de las tareas del curso —centradas en el problema de *churn*—, el proyecto final aborda un **problema aplicado de riesgo socioambiental**, integrando datos satelitales y variables climáticas actuales y rezagadas, con el objetivo de apoyar la **gestión del riesgo y la toma de decisiones operativas**.

---

## Enfoque del proyecto

El proyecto se basa en la hipótesis de que la intensidad extrema de los incendios forestales no depende únicamente de condiciones meteorológicas instantáneas, sino que responde a **procesos acumulativos** asociados a la llamada *memoria climática*.  

Para capturar este fenómeno, se utilizan:
- Variables meteorológicas actuales y rezagadas (temperatura, humedad relativa, viento y precipitación).
- Información energética inicial del incendio (Fire Radiative Power, FRP).
- Un enfoque de **clasificación binaria**, donde se identifican incendios severos definidos por un umbral de **FRP ≥ 100 MW**, ampliamente utilizado en la literatura y en contextos operativos.

---

## Contenido del directorio

### `Paper.pdf`
Documento principal del proyecto.  
Corresponde al artículo académico donde se describe en detalle:
- El contexto del problema.
- El planteamiento de investigación.
- Los objetivos e hipótesis.
- El diseño experimental y el flujo metodológico.
- El modelamiento predictivo basado en **Random Forest**.
- El análisis de resultados, discusión y conclusiones.

Este documento constituye la **síntesis formal del proyecto final**.

---

### `Datasets_base`
Contiene los **datasets utilizados como insumo** para el desarrollo del proyecto.  
Incluye información derivada de detecciones satelitales de incendios y variables meteorológicas asociadas, que posteriormente son procesadas para reconstruir eventos de incendio únicos y generar variables climáticas rezagadas.

---

### `Modelos`
Carpeta destinada a almacenar **modelos entrenados**, resultados intermedios y artefactos derivados del proceso de modelamiento.  
Su propósito es facilitar la reproducibilidad, el análisis comparativo y la extensión futura del trabajo.

---

## Metodología general

El proyecto sigue un flujo metodológico estructurado que incluye:
- Reconstrucción de eventos de incendio mediante agrupación espacio-temporal.
- Generación de variables climáticas rezagadas para capturar efectos acumulativos.
- Manejo explícito del **desbalance de clases**, priorizando la detección de eventos severos.
- Evaluación con métricas adecuadas para escenarios de riesgo, como **recall**, **F1** y análisis del trade-off entre sensibilidad y precisión.
- Interpretación del modelo mediante análisis de **importancia de variables**, vinculando los resultados con procesos físicos subyacentes.

---

## Relación con las tareas del curso

-  **Tareas**: se centran en el problema de *churn* y cumplen un rol formativo, explorando progresivamente distintos modelos de Machine Learning.
-  **Proyecto final**: aplica los conceptos aprendidos a un **caso real y contextualizado**, con un enfoque investigativo y aplicado.

