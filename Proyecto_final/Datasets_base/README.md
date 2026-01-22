# Datasets_base

Este directorio contiene los **datasets base y notebooks de preprocesamiento** utilizados en el proyecto final de Machine Learning II.  
Aquí se concentran los insumos fundamentales a partir de los cuales se construyen los datasets finales para el análisis y modelamiento de incendios forestales.

El contenido de este directorio corresponde a la **fase inicial del pipeline de datos**, donde se integran y transforman fuentes climáticas y de incendios satelitales.

---

## Estructura del directorio

```
Datasets_base/
│
├── Dataset_clima/
│   ├── Condiciones_Climáticas_Biobio_2020_2024.csv
│   ├── Obtener_Registros_Clima.ipynb
│   └── README.md
│
├── Datasets_incendios/
│   ├── viirs-snpp_2020_Chile.csv
│   ├── viirs-snpp_2021_Chile.csv
│   ├── viirs-snpp_2022_Chile.csv
│   ├── viirs-snpp_2023_Chile.csv
│   ├── viirs-snpp_2024_Chile.csv
│   ├── Crear_dataset_incendios.ipynb
│   └── README.md
│
├── Unir_incendios_con_clima.ipynb
│
└── Crear_eventos.ipynb
```

---

## Dataset_clima

Contiene el **dataset climático histórico** para la Región del Biobío (2020–2024), junto con el notebook utilizado para su obtención y consolidación desde fuentes meteorológicas externas.

Este dataset constituye la base para la caracterización de las condiciones ambientales asociadas a la ocurrencia de incendios forestales.

El detalle del contenido y las variables se encuentra documentado en `Dataset_clima/README.md`.

---

## Datasets_incendios

Incluye los **datasets de focos de incendios forestales en Chile**, obtenidos a partir de detecciones satelitales VIIRS (Suomi NPP), organizados por año.

Además, contiene un notebook destinado a la unión y consolidación de los registros anuales en un único dataset de incendios.

El detalle del contenido y las variables se encuentra documentado en `Datasets_incendios/README.md`.

---

## Unir_incendios_con_clima.ipynb

Notebook encargado de realizar la **integración espacio-temporal entre los datos climáticos y los focos de incendio**.

El proceso está documentado por etapas directamente en el código, lo que asegura trazabilidad y claridad metodológica.

Resultado: dataset detallado que combina clima e incendios, incluyendo días con y sin eventos.

---

## Crear_eventos.ipynb

Notebook destinado a la **construcción de eventos de incendio y variables derivadas**, a partir del dataset integrado clima–incendios.

Incluye procesos de limpieza, agregación temporal y espacial, cálculo de métricas de intensidad (FRP) y generación de variables para análisis y modelamiento.

Resultado: dataset agregado a nivel de evento, listo para análisis exploratorio y modelos de aprendizaje automático.

---

## Alcance del directorio

El contenido de `Datasets_base` representa la **base del pipeline de datos del proyecto**, y está orientado a:

- Garantizar trazabilidad y reproducibilidad.
- Facilitar la integración entre clima e incendios.
- Proveer insumos consistentes para análisis exploratorio y modelamiento predictivo.
- Servir como respaldo metodológico del proceso de construcción de los datasets finales.
