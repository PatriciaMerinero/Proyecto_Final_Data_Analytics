




# Proyecto_final_Data_Analytics
Proyecto final del *Máster en Data Analytics*, centrado en el análisis exploratorio de un conjunto de datos bancarios sintéticos mediante Python.  
El trabajo se estructura en varios notebooks (EDA preliminar, limpieza, análisis descriptivo e informe) y se complementa con un dashboard en Power BI.



**Título del proyecto:** Análisis de fraudes en transacciones bancarias  
**Autor:** Patricia Merinero  
**Fecha:** Noviembre 2025  


## 📂 Estructura del proyecto


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



## 🧭 1. Objetivo del proyecto  
Este proyecto tiene como objetivo analizar un conjunto de datos de transacciones financieras de clientes, con foco en la detección de patrones de fraude.  
Se busca responder preguntas como:  
- ¿Qué variables explican mejor las operaciones fraudulentas?  
- ¿Existen diferencias geográficas o temporales en los fraudes?  
- ¿Cómo se comportan los clientes con mayor nivel de riesgo?

---

## 2. Estructura



<img width="406" height="173" alt="image" src="https://github.com/user-attachments/assets/7a87787a-b311-4883-8f8d-c5e47bf689f6" />




---

## 🧹 3. Limpieza y Transformación de datos  
En esta fase se ejecutó el flujo completo de transformación de los datos para dejarlos listos para el análisis exploratorio y la visualización.

**Pasos principales:**
1. Identificadores y trazabilidad: revisión de `transaction_id`, `customer_id`.  
2. Datos financieros y de transacción: limpieza de `amount`, `currency`.  
3. Información del comercio y categoría: normalización de `merchant`, `merchant_category`.  
4. Información del cliente y contacto: limpieza de `name`, `email`, `phone`.  
5. Geolocalización: normalización de `region_normalized` (cliente) y `country_normalized` (transacción), creación de `is_international`.  
6. Temporalidad de las transacciones: transformación de `transaction_time`, creación de `transaction_date`, `transaction_hour`, `hour`, `year`, `month`, `day`, `weekday`, `month_year`.  
7. Antigüedad de los clientes (`customer_days_active`): cálculo de cuántos días lleva activo el cliente.  
7.1 Unificación y orden de columnas: reorganización del dataset en bloques temáticos.  
8. Exportación final: guardado del dataset limpio en `DATA_OUTPUT` listo para el EDA.

---

## 📊 4. Análisis Exploratorio de Datos (EDA)  
*(Aquí añadirás más adelante los resultados principales, gráficos y hallazgos)*
---


### 🔄 5. Actualización de datasets iniciales (08/11/2025)
- Se han reemplazado los archivos originales `clientes_sinteticos.csv` y `transacciones_sinteticas.csv` por versiones ampliadas con mayor número de filas (≈65.000 en total).  
- Se mantiene la misma estructura de columnas, tipología de datos y consistencia relacional.  
- El reemplazo garantiza el cumplimiento del requisito mínimo de tamaño del conjunto de datos (>50.000 filas).

---

## 🚀 6. Cómo ejecutar este proyecto  

1️⃣ Clona el repositorio:

https://github.com/PatriciaMerinero/Proyecto_Final_Data_Analytics.git

2️⃣ Crea y activa un entorno virtual (por ejemplo usando venv).

🟢 entorno: entorno_proyecto_final
🐍 versión: Python 3.13.8

3️⃣ Instala dependencias:

pip install -r requirements.txt

4️⃣ Abre los notebooks en la carpeta NOTEBOOKS y ejecútalos en orden:

01_EDA_PRELIMINAR.ipynb

02_EDA_LIMPIEZA_TRANSFORMACION.ipynb






   

