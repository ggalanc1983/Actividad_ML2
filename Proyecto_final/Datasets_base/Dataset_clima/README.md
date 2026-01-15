# Dataset Climático – Región del Biobío (2020–2024)

Este directorio contiene un **dataset climático histórico consolidado** para la **Región del Biobío**, correspondiente al período **2020–2024**.

El dataset ha sido elaborado a partir de datos meteorológicos agregados y está orientado a su uso en **análisis ambientales, estudios climáticos y modelamiento predictivo**, especialmente para investigaciones relacionadas con **incendios forestales**.

---

## Contenido del directorio

- `Condiciones_Climáticas_Biobio_2020_2024.csv`  
  Dataset climático histórico con variables meteorológicas diarias asociadas a comunas de la Región del Biobío.

- `Obtener_Registros_Clima.ipynb`
  Archivo en python para obtención de histórico de condiciones climáticas desde API de open-meteo

- `README.md`  
  Documento descriptivo del contenido, estructura y uso del dataset.

  

---

## Variables incluidas

El dataset contiene las siguientes columnas:

| Variable | Descripción |
|--------|-------------|
| `date` | Fecha de registro (YYYY-MM-DD) |
| `temperature_2m_mean` | Temperatura media diaria a 2 metros (°C) |
| `relativehumidity_2m_mean` | Humedad relativa media diaria (%) |
| `precipitation_sum` | Precipitación diaria acumulada (mm) |
| `windspeed_10m_mean` | Velocidad media del viento a 10 m (km/h o m/s según fuente) |
| `winddirection_10m_mean` | Dirección media del viento a 10 m (grados) |
| `comuna` | Comuna asociada al registro climático |
| `provincia` | Provincia correspondiente |
| `region` | Región administrativa (Biobío) |
| `latitud` | Latitud geográfica del punto representativo |
| `longitud` | Longitud geográfica del punto representativo |

---

## Resolución y cobertura

- **Resolución temporal:** diaria  
- **Cobertura temporal:** 2020 – 2024  
- **Cobertura espacial:** comunas de la Región del Biobío  
- **Tipo de datos:** variables meteorológicas agregadas

---

## Uso previsto

Este dataset está diseñado para:

- Integración con datasets de incendios forestales (VIIRS S-NPP, MODIS)
- Análisis exploratorio de condiciones climáticas (EDA)
- Generación de variables rezagadas (lags climáticos)
- Entrenamiento de modelos de Machine Learning
- Estudios académicos, tesis de magíster y proyectos de investigación aplicada

---

## Consideraciones importantes

- Los datos corresponden a **valores agregados**, no a mediciones directas de estaciones en terreno.
- Pueden existir valores faltantes o estimados según disponibilidad de la fuente original.
- Se recomienda realizar procesos de:
  - Limpieza de datos
  - Validación temporal y espacial
  - Normalización o estandarización antes de su uso en modelos predictivos.

---

## Contexto del proyecto

Este directorio forma parte de la actividad **ML2 – Datasets base**, enfocada en el análisis conjunto de **variables climáticas e incendios forestales**, como apoyo al desarrollo de modelo

