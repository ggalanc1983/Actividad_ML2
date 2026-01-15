# Datasets de Clima e Incendios Forestales – Pipeline de Procesamiento

Este directorio contiene los **tres datasets generados de forma secuencial** durante el proceso de integración, transformación y depuración de datos climáticos y de incendios forestales en Chile.  
Cada archivo representa una **etapa distinta del pipeline**, desde datos diarios comunales hasta incendios físicos consolidados, listos para análisis y modelado predictivo.

---

## Estructura del Directorio

```
/datasets
│
├── Dataset_Clima_Incendios_Diario_Comunal.csv
├── Dataset_Eventos_Incendio_Clima_Lags.csv
└── Dataset_Incendios_Fisicos_Depurado.csv
```

---

## Dataset_Clima_Incendios_Diario_Comunal.csv  
**Nivel:** Diario – Comunal  

### Descripción
Dataset base que integra **variables climáticas diarias** con **detecciones de incendios satelitales**, asignando cada incendio a la comuna más cercana.  
Incluye explícitamente **días con y sin incendios**, permitiendo análisis balanceados y temporales.

### Características principales
- Unidad temporal: **día**
- Unidad espacial: **comuna**
- Asignación espacial de incendios por distancia geográfica
- Inclusión de días sin incendios
- Clasificación inicial de incendios según FRP
- Variables binarias (ocurrencia, intensidad, día/noche)

---

## Dataset_Eventos_Incendio_Clima_Lags.csv  
**Nivel:** Evento de incendio  

### Descripción
Dataset transformado a **nivel de evento**, donde las detecciones satelitales se agrupan espacial y temporalmente para representar **incendios individuales**.  
Se incorporan **variables climáticas históricas (lags)** y métricas de evolución del fuego.

### Características principales
- Agrupación espacial (~1 km) y temporal (≤ 24 h)
- Cálculo de métricas por evento:
  - FRP inicial y máximo
  - Duración del incendio
  - Incremento de intensidad (ΔFRP)
- Variables climáticas rezagadas (1, 2 y 3 días)
- Definición de target supervisado (`target_transicion`)

---

## Dataset_Incendios_Fisicos_Depurado.csv  
**Nivel:** Incendio físico real (final)  

### Descripción
Dataset final depurado que consolida **eventos fragmentados** en **incendios físicos reales**, utilizando criterios de proximidad espacial y temporal.  
Elimina eventos espurios y recupera variables climáticas representativas.

### Características principales
- Fusión de eventos cercanos:
  - Misma comuna
  - Diferencia temporal ≤ 24 h
  - Distancia ≤ 1.5 km
- Eliminación de incendios con duración 0
- Reagregación final de métricas del incendio
- Integración de clima histórico definitivo
- Dataset limpio y consistente para modelado final
  
---

## Relación entre los datasets (Pipeline)

```
Dataset_Clima_Incendios_Diario_Comunal
              ↓
Dataset_Eventos_Incendio_Clima_Lags
              ↓
Dataset_Incendios_Fisicos_Depurado
```

Cada dataset **depende directamente del anterior** y representa una etapa más avanzada de procesamiento y limpieza.

---

## Notas adicionales
- Todos los datasets están en formato CSV.
- Codificación compatible con Excel y Python.
- Pensados para uso en **Python, R o software estadístico**.
- El dataset final es el recomendado para entrenamiento de modelos.
