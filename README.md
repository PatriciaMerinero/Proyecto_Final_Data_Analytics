




#  Proyecto_final_Data_Analytics
Proyecto final del *Máster en Data Analytics*, centrado en el análisis exploratorio de un conjunto de datos bancarios sintéticos mediante Python.  
El trabajo se estructura en varios notebooks (EDA preliminar, limpieza, análisis descriptivo e informe) y se complementa con un dashboard en Power BI.



## 1. 💳 **Título del proyecto:** Análisis de fraudes en transacciones bancarias  
**Autor:** Patricia Merinero  
**Fecha:** Noviembre 2025  

---
---


## 2. 📝 Descripción del proyecto

Este proyecto forma parte del **Proyecto Final del Máster en Data Analytics** y tiene como objetivo analizar un conjunto de datos sintéticos de **clientes** y **transacciones financieras** para obtener una visión clara del comportamiento de los clientes y del **riesgo de fraude en las operaciones**.

A partir de los ficheros originales (`clientes_sinteticos.csv` y `transacciones_sinteticas.csv`), se construye un flujo de trabajo completo de **análisis exploratorio de datos (EDA)** en Python y un **dashboard interactivo en Power BI** que permite a perfiles no técnicos explorar los resultados de forma visual.


---
### 📊 Objetivo principal

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


PROYECTO_FINAL_DATA_ANALYTICS/
│
├── DATA/
│   ├── DATA_OUTPUT/
│   │   ├── dataset_limpio_y_transformado.csv
│   │   └── datos_unidos.csv
│   │
│   ├── EDA/
│   │   ├── amount_por_risk_level.csv
│   │   ├── comparativa_fraude.csv
│   │   ├── distribución_fraude_mes.png
│   │   ├── fraud_por_tipo_tarjeta.png
│   │   ├── Operaciones_fraude_dia_mes.png
│   │   ├── tasa_fraude_topN_merchant.png
│   │   └── *todas las gráficas generadas durante el análisis exploratorio*
│   │
│   └── DATA_RAW/
│       ├── clientes_sinteticos.csv
│       └── transacciones_sinteticas.csv
│
├── INFORME/
│   └── 04_INFORME.pdf
│
├── NOTEBOOKS/
│   ├── 01_EDA_PRELIMINAR.ipynb
│   ├── 02_EDA_LIMPIEZA_TRANSFORMACION.ipynb
│   ├── 03_EDA_ANALISIS_DESCRIPTIVO.ipynb
│   └── 04_INFORME.ipynb
│
├── POWER BI/
│   └── PROYECTO_FINAL_VISUALIZACION_POWERBI.pbix
│
├── .gitignore
├── README.md
└── requirements.txt

```

## 4. 🛠️ Instalación y requisitos

Este proyecto se puede ejecutar en cualquier equipo que tenga instalado Python y Power BI.  
A continuación se detalla todo lo necesario para reproducir el análisis y el dashboard.


---

### 4.1. ✔ Software necesario

Para ejecutar correctamente el proyecto se deben instalar:

- **Python 3.10 o superior**
- **Visual Studio Code**
  - Extensión: *Python*
  - Extensión: *Jupyter*
- **Power BI Desktop** (para abrir el dashboard `.pbix`)
- **Git** (opcional, si deseas clonar el repositorio)

---

### 4.2. ✔ Clonar o descargar el proyecto

Si está disponible en GitHub:

```bash
git clone https://github.com/PatriciaMerinero/Proyecto_Final_Data_Analytics.git


```

### 4.3. ✔ Activar el entorno virtual

Antes de instalar las dependencias, activa el entorno virtual del proyecto:

**Windows**
```bash
entorno_proyecto_final\Scripts\activate

```
### 4.4  ✔  Instalación de dependencias

Antes de ejecutar los notebooks, instala las librerías necesarias con:

```bash
pip install -r requirements.txt


> Nota: El archivo `requirements.txt` ha sido generado automáticamente con  
> `pip freeze` desde el entorno virtual del proyecto, tal y como se recomienda  
> en las buenas prácticas de reproducibilidad.

```
### 4.5 ✔  Registrar el entorno como kernel de Jupyter

Para que Visual Studio Code o Jupyter Notebook puedan ejecutar las celdas usando este entorno virtual, es necesario instalar y registrar el paquete ipykernel.

Después, registra el entorno como kernel disponible

```bash
pip install ipykernel


python -m ipykernel install --user --name entorno_proyecto_final --display-name "Python (entorno_proyecto_final)"

---
---
```
## 5. 🎯Resultados y conclusiones

### 5.1 Resumen de hallazgos clave

- **Fraude global y distribución temporal**
  - La tasa global de fraude es baja (≈1,10 %), pero **no se distribuye de forma uniforme en el tiempo**.
  - Se observan **picos a inicios y finales de mes** y en franjas horarias concretas (≈2–3 h de la madrugada y alrededor de las 15 h), lo que sugiere momentos de mayor exposición al riesgo.

- **Canales de entrada (entry_mode)**
  - **wallet** es el canal con **mayor frecuencia de uso** y **mayor tasa de fraude**, lo que lo convierte en un foco prioritario de vigilancia.
  - **magstripe** y **contactless** tienen una tasa de fraude moderada pero se usan mucho, por lo que su exposición agregada es relevante.
  - **chip (EMV)** es el canal **más seguro**, con la menor tasa de fraude, en línea con la tecnología más robusta que utiliza.

- **Tipo de tarjeta (card_type)**
  - **AMEX** y **MASTERCARD** presentan las **tasas de fraude más altas**, mientras que **VISA** muestra la **más baja**.
  - Esto apunta a diferencias en la combinación de perfil de cliente, tipo de comercio y políticas de control de cada red.

- **Tipo de comercio y geografía**
  - Algunas **categorías de comercio** concentran más fraude (por volumen o por tasa relativa), lo que permite identificar **sectores más sensibles**.
  - A nivel geográfico, países como **Spain**, **Netherlands Antilles** o **China** muestran **tasas de fraude superiores a la media**, indicando contextos donde conviene reforzar controles.

- **Resultado de la transacción (transaction_result)**
  - Las **transacciones declinadas** concentran la **mayor tasa de fraude**, lo que indica que los filtros antifraude están funcionando y bloquean muchos intentos.
  - Las **transacciones aprobadas** tienen la menor tasa, pero aún contienen un fraude residual (≈1 %), que justifica reforzar la monitorización post-autorización.

- **Risk score y niveles de riesgo**
  - El análisis por **deciles de risk_score** y **risk_level** muestra que la tasa de fraude **no crece de forma perfectamente monótona**.
  - Esto sugiere que el modelo de scoring podría beneficiarse de **recalibración** o incorporación de nuevas variables para mejorar su capacidad de discriminación.

En conjunto, el análisis confirma que el fraude se concentra en **ciertos canales, franjas horarias, tipos de tarjeta, países y categorías de comercio**, y que el **risk_score actual es razonablemente útil**, pero con margen de mejora.

---

### 5.2 Gráficos y tablas recomendados para el README

Para ilustrar los resultados más relevantes en el README, se recomienda incluir (o al menos referenciar) los siguientes recursos generados en `DATA/DATA_OUTPUT/EDA`:

- **Distribución temporal y picos de fraude**
  - `Operaciones_fraudulentas_dia.png`  
    Muestra la evolución diaria del fraude y ayuda a visualizar los picos de actividad.
  - `Operaciones_fraudulentas_hora_dia.png`  
    Refuerza las conclusiones sobre horas críticas (2–3 h y 15 h).

- **Canales y tarjetas**
  - `Distribucion_general_entry_mode.png` + gráfico de **tasa de fraude por entry_mode**  
    Permiten explicar la combinación de **popularidad vs. riesgo** de cada canal (wallet, contactless, chip, etc.).
  - `fraude_por_tipo_tarjeta.png`  
    Resume la **tasa de fraude por tipo de tarjeta** (VISA, MASTERCARD, AMEX, DISCOVER).

- **Comercios y geografía**
  - `tasa_fraude_topN_merchant.png`  
    Destaca los comercios con **mayor tasa relativa de fraude**, útil para priorizar revisiones.
  - `top_paises_volumen_operaciones_fraude.png`  
    Apoya las conclusiones sobre **países con mayor exposición**.
  - `geo_risk_score_violin.png`  
    Muestra la distribución del **risk_score por región/país**, visualizando zonas de mayor riesgo.

- **Resultado de la transacción y score**
  - `fraude_por_resultado_transaccion.png`  
    Ilustra la diferencia entre **fraude en aprobadas, pendientes y declinadas**.
  - `amount_por_risk_level.png` y/o tabla `resumen_estadistico.csv`  
    Complementan el análisis de **niveles de riesgo** y su relación con importe y fraude.

En el README se pueden incluir las imágenes más representativas (por ejemplo, 4–6 gráficos clave) y dejar el resto como **recursos adicionales** referenciados.

---

### 5.3 Utilidad de los resultados para usuarios y tomadores de decisiones

Los resultados de este proyecto son útiles para distintos perfiles dentro de un entorno de **fraude y riesgo**:

- **Equipos de fraude / riesgo operativo**
  - Pueden **priorizar controles** en:
    - canales de entrada más expuestos (wallet, magstripe),
    - franjas horarias críticas,
    - países y comercios con mayor tasa de fraude.
  - Obtienen una guía clara sobre **dónde reforzar reglas, límites y revisiones manuales**.

- **Data analysts / data scientists**
  - Disponen de un **dataset limpio, documentado y enriquecido**, listo para:
    - entrenar modelos de clasificación de fraude,
    - recalibrar el **risk_score**,
    - diseñar nuevas features basadas en tiempo, geografía, canal, etc.

- **Gestores de negocio y producto**
  - Pueden entender, en lenguaje claro, **cómo se comporta el fraude** por canal, tarjeta, país y sector.
  - Tienen argumentos cuantitativos para:
    - ajustar políticas comerciales (p. ej. límites por país o canal),
    - negociar con redes de tarjeta o procesadores,
    - planificar recursos de monitorización en los periodos de mayor riesgo.

- **Stakeholders no técnicos**
  - Gracias a los gráficos y resúmenes, pueden **visualizar rápidamente**:
    - dónde está el problema,
    - qué canales son más seguros o más vulnerables,
    - cómo evoluciona el fraude en el tiempo.
  - Esto facilita la toma de decisiones basada en datos y la priorización de iniciativas de mejora.

En resumen, los resultados del EDA no solo describen el comportamiento del fraude, sino que proporcionan una **base accionable** para mejorar la prevención, la gestión operativa y la evolución futura del modelo de riesgo.










