# Datasets de Incendios Forestales – Chile (VIIRS S-NPP)

Este directorio contiene un conjunto de **datasets base de incendios forestales en Chile**, obtenidos a partir de detecciones satelitales **VIIRS (Visible Infrared Imaging Radiometer Suite)** del satélite **Suomi NPP**.

Los archivos están organizados por año y están diseñados para ser utilizados como insumo en **análisis exploratorios, modelamiento predictivo y estudios de aprendizaje automático (ML)** relacionados con incendios forestales.

---

## Contenido del directorio

Cada archivo CSV corresponde a un año específico de detecciones de incendios en Chile:

- `viirs-snpp_2020_Chile.csv`
- `viirs-snpp_2021_Chile.csv`
- `viirs-snpp_2022_Chile.csv`
- `viirs-snpp_2023_Chile.csv`
- `viirs-snpp_2024_Chile.csv`

Los datasets incluyen información espacial, temporal y radiométrica asociada a focos de incendio detectados por sensores satelitales.

- `Crear_dataset_incendios.ipynb`

Script en Python que realiza la unión en un solo archivo de los registros anuales.


---

## Uso previsto

Estos datos pueden ser utilizados para:

- Análisis exploratorio de incendios forestales (EDA)
- Modelos de clasificación y predicción de intensidad de incendios
- Integración con variables meteorológicas (Open-Meteo, NASA GEOS, etc.)
- Estudios académicos, tesis o proyectos de investigación
- Visualizaciones geoespaciales y análisis temporal

---

## Consideraciones importantes

- Los datos provienen de **detecciones satelitales**, por lo que representan **puntos de calor** y no necesariamente incendios confirmados en terreno.
- Se recomienda realizar procesos de **limpieza, filtrado espacial y validación** antes de su uso en modelos predictivos.
- La resolución temporal y espacial depende de las condiciones de paso del satélite.

---

## Contexto del proyecto

Este directorio forma parte de la actividad **ML2 – Datasets base**, enfocada en el estudio de incendios forestales y su relación con variables climáticas y ambientales, como apoyo a modelos de aprendizaje automático.

---

## Uso académico

Repositorio utilizado con fines **educativos y de investigación**. 


