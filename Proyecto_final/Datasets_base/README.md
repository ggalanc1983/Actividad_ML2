# 📊 Datasets y Notebooks de Clima e Incendios Forestales – Pipeline de Procesamiento

Este directorio contiene los **datasets y notebooks de Google Colab** generados de forma secuencial durante el proceso de integración, transformación y depuración de datos climáticos y de incendios forestales en Chile.  
Cada archivo representa una **etapa distinta del pipeline**, desde datos diarios comunales hasta incendios físicos consolidados, listos para análisis y modelado predictivo.

---

## 🧩 Estructura del Directorio

```
/datasets
│
├── Clima_Incendios_Detallado_Clasificado.csv
├── Dataset_Incendios_y_clima_Final.csv
├── Dataset_Incendios_Eventos_Fusionados_SinDuracionCero.csv
│
├── Unir_incendios_con_clima.ipynb
├── Crear_Dataset_final_incendios.ipynb
└── Limpiar_dataset.ipynb
```

---

## 🔹 Notebooks (Google Colab)

Estos notebooks implementan el pipeline completo de procesamiento de datos.  
Deben ejecutarse **en el orden indicado**, ya que cada uno depende de la salida del anterior.

### 1️⃣ Unir_incendios_con_clima.ipynb
- Integra datos climáticos diarios con detecciones de incendios satelitales.
- Asigna incendios a comunas mediante distancia geográfica.
- Incorpora días sin incendios.
- Genera variables de clasificación inicial y variables binarias.

📤 **Dataset generado:**  
`Clima_Incendios_Detallado_Clasificado.csv`

---

### 2️⃣ Crear_Dataset_final_incendios.ipynb
- Agrupa detecciones satelitales en eventos de incendio.
- Calcula métricas por evento (FRP inicial, máximo, duración).
- Incorpora variables climáticas históricas (lags).
- Define el target supervisado de transición del incendio.

📤 **Dataset generado:**  
`Dataset_Incendios_y_clima_Final.csv`

---

### 3️⃣ Limpiar_dataset.ipynb
- Detecta y fusiona eventos fragmentados espacial y temporalmente.
- Consolida incendios físicos reales.
- Elimina eventos con duración cero.
- Recupera variables climáticas representativas.
- Genera el dataset final depurado.

📤 **Dataset generado:**  
`Dataset_Incendios_Eventos_Fusionados_SinDuracionCero.csv`

---

## 🔗 Relación entre los datasets (Pipeline)

```
Unir_incendios_con_clima.ipynb
              ↓
Clima_Incendios_Detallado_Clasificado.csv
              ↓
Crear_Dataset_final_incendios.ipynb
              ↓
Dataset_Incendios_y_clima_Final.csv
              ↓
Limpiar_dataset.ipynb
              ↓
Dataset_Incendios_Eventos_Fusionados_SinDuracionCero.csv
```

---

## 🧪 Notas adicionales
- Todos los datasets están en formato CSV.
- Los notebooks están pensados para ejecutarse en **Google Colab**.
- Codificación compatible con Excel, Python y R.
- El dataset final es el recomendado para entrenamiento de modelos predictivos.
