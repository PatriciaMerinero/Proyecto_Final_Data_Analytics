# Proyecto_final_Data_Analytics
Exploratory Data Analysis (EDA) sobre detección de fraude financiero, combinando información de clientes y transacciones para identificar patrones sospechosos mediante Python y visualización de datos.

**Título del proyecto:** Análisis de fraudes en transacciones bancarias  
**Autor:** Patricia Merinero  
**Fecha:** Noviembre 2025  

---

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

## 🚀 5. Cómo ejecutar este proyecto  
1. Clona el repositorio:  
   ```bash
   git clone https://github.com/PatriciaMerinero/Proyecto_Final_Data_Analytics.git

