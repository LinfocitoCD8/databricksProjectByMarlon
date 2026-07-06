# ETL DATOS DE SUPERMERCADO: PRODUCTOS, TRANSACCIONES Y DEMAS
Arquitectura Medallion en Azure Databricks  
Pipeline automatizado de datos para el analisis de datos de un supermercado, utilizando arquitectura de tres capas y un despliegue CI/CD
# - Descripcion del proyecto
Se creo un pipeline de Extraccion, Transformacion y Carga (ETL), en donde tomaremos datos crudos del supermercado, los ingresaremos dentro de una arquitectura Medallion (Bronze, Silver, Golden) en Azure Databricks. 
El almacenamiento de los archivos crudos se encontraran en Azure Data Lake. Desde Databricks tomaremos estos datos y realizaremos todo el proceso automatizado con CI/CD. 
Implementamos tambien el manejo de permisos (GRANTS), teniendo un enfoque de gobernanza de datos en el proceso. 
# - Flujo de los datos
Datos crudos (DATA LAKE HOUSE)
↓
Bronze(Ingesta)

↓
Silver(Limpieza + transformacion)
↓
Golden(Datos listos para desplegar)
↓
Dashboards (Visualizaciones simples usando Power BI)
<img width="483" height="265" alt="ImagenReadme" src="https://github.com/user-attachments/assets/88749655-2c23-4bfe-949a-853a5a56c07d" />





