




#  Proyecto_final_Data_Analytics
Proyecto final del *Máster en Data Analytics*, centrado en el análisis exploratorio de un conjunto de datos bancarios sintéticos mediante Python.  
El trabajo se estructura en varios notebooks (EDA preliminar, limpieza, análisis descriptivo e informe) y se complementa con un dashboard en Power BI.



## 1. **Título del proyecto:** Análisis de fraudes en transacciones bancarias  
**Autor:** Patricia Merinero  
**Fecha:** Noviembre 2025  

---
---


## 2. 📝 Descripción del proyecto

Este proyecto forma parte del **Proyecto Final del Máster en Data Analytics** y tiene como objetivo analizar un conjunto de datos sintéticos de **clientes** y **transacciones financieras** para obtener una visión clara del comportamiento de los clientes y del **riesgo de fraude en las operaciones**.

A partir de los ficheros originales (`clientes_sinteticos.csv` y `transacciones_sinteticas.csv`), se construye un flujo de trabajo completo de **análisis exploratorio de datos (EDA)** en Python y un **dashboard interactivo en Power BI** que permite a perfiles no técnicos explorar los resultados de forma visual.


---
### 🎯 Objetivo principal

El objetivo del proyecto es:

> **Detectar patrones de comportamiento y riesgo en las transacciones, con especial foco en el fraude, para apoyar la toma de decisiones en un contexto similar al de una entidad financiera.**

Para ello se:
- Unifican y transforman las bases de datos de clientes y transacciones.
- Analizan las **características de los clientes**, las **operaciones** y las **variables asociadas al fraude**.
- Diseñan **KPIs y visualizaciones** que permiten entender:
  - el riesgo por **país del comercio**,
  - el perfil de la operación por **modo de entrada**,  
  - y el **perfil del cliente** asociado al fraude.

---
### 🧩 Problema que aborda

En un entorno de pagos, los datos suelen estar **dispersos** entre varias fuentes (clientes, transacciones, atributos de riesgo…), lo que dificulta:

- Tener una **visión consolidada** del comportamiento del cliente.
- Medir correctamente la **tasa e impacto del fraude**.
- Detectar segmentos, países o modos de entrada con **mayor concentración de riesgo**.

Este proyecto simula ese escenario y propone una solución basada en:

- Un **dataset unificado y limpio** (`datos_unidos.csv` y `dataset_limpio_y_transformado.csv`).
- Un **análisis descriptivo** estructurado.
- Un **dashboard** que responde a preguntas clave como:
  - ¿En qué países se concentra más el fraude?
  - ¿Qué modos de entrada de la operación presentan mayor riesgo?
  - ¿Qué tipo de clientes están más expuestos al fraude?

---

### 🛠️ Técnicas y enfoques utilizados

Para llevar a cabo el análisis se ha seguido un enfoque **paso a paso**, estructurado en distintos notebooks:

#### ▸ Integración y preparación de datos
- Unión de bases de clientes y transacciones.
- Revisión de tipos de datos (fechas, numéricos, categóricos).
- Tratamiento de **valores nulos**, **duplicados** y registros inconsistentes.
- Creación de variables derivadas (categorías de ingresos, indicadores de fraude, agrupaciones geográficas, etc.).

#### ▸ Análisis exploratorio y descriptivo (EDA)
- Estadísticos descriptivos (medias, medianas, percentiles, distribución de importes).
- Análisis univariante y bivariante por:
  - país del comercio,
  - modo de entrada de la operación,
  - características del cliente.
- Cálculo de métricas clave:
  - **tasa de fraude**,
  - **importe total y medio de fraude**,
  - distribución del fraude por país, modo de entrada y perfil de cliente.

#### ▸ Visualización y dashboard
- Generación de gráficos exploratorios en Python.
- Definición de **KPIs** relevantes para negocio.
- Construcción de un **dashboard en Power BI** que permite:
  - filtrar por país, modo de entrada y características del cliente,
  - visualizar mapas de riesgo,
  - comparar volumen e importe de fraude entre segmentos.

---

En conjunto, el proyecto muestra cómo pasar de **datos en bruto** a **insights accionables**, utilizando técnicas de análisis exploratorio, tratamiento de datos y visualización orientadas específicamente al contexto de **fraude en transacciones financieras**.

---
---

## 📂 3. Estructura del proyecto


```text
PROYECTO_FINAL
├──PROYECTO_FINAL_VISUALIZACION_POWERBI.pbix

PROYECTO_FINAL_DATA_ANALYTICS/
├── DATA/
│   ├── DATA_RAW/
│   │   ├── clientes_sinteticos.csv
│   │   └── transacciones_sinteticas.csv
│   │
│   └── DATA_OUTPUT/
│       └── EDA/
│           ├── datos_unidos.csv
│           └── dataset_limpio_y_transformado.csv
│
├── NOTEBOOKS/
│   ├── 01_EDA_PRELIMINAR.ipynb
│   ├── 02_EDA_LIMPIEZA_TRANSFORMACION.ipynb
│   ├── 03_EDA_ANALISIS_DESCRIPTIVO.ipynb
│   └── 04_INFORME.ipynb
│
├── entorno_proyecto_final/        # Entorno virtual (excluido en .gitignore)
├── .gitignore
├── README.md



