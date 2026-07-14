# ETL DATOS DE SUPERMERCADO: PRODUCTOS, TRANSACCIONES Y DEMAS
Arquitectura Medallion en Azure Databricks  
Pipeline automatizado de datos para el analisis de datos de un supermercado, utilizando arquitectura de tres capas y un despliegue CI/CD
# 🚀 Descripción del proyecto
Pipeline automatizado de Extracción, Transformación y Carga (ETL) para análisis de datos de un supermercado, implementado en Azure Databricks bajo la arquitectura Medallion (Bronze, Silver, Gold).
El proyecto incluye:

- Almacenamiento de datos crudos en Azure Data Lake
 
- Procesamiento y transformación en Databricks

- Despliegue automatizado con CI/CD

- Gobernanza de datos mediante GRANTS

- Orquestacion mediante pipeline en Databricks workflow

- Visualización con Power BI
#🎯 Objetivos
Centralizar y limpiar datos de productos y transacciones.

Implementar un flujo de datos confiable y escalable.

Facilitar la creación de dashboards para análisis de negocio.

Garantizar seguridad y gobernanza en el acceso a los datos.

# 🗂️ Flujo de datos
Datos crudos → Data Lakehouse

Bronze → Ingesta

Silver → Limpieza + Transformación

Gold → Datos listos para consumo

Dashboards → Visualizaciones en Power BI

<img width="483" height="265" alt="ImagenReadme" src="https://github.com/user-attachments/assets/88749655-2c23-4bfe-949a-853a5a56c07d" />

# 🛠️ Tecnologías utilizadas
Azure Databricks

Azure Data Lake

Power BI

CI/CD con GitHub Actions / Azure DevOps

PySpark / SQL

# ## 📁 Estructura del repositorio

- **/datasets** → insumos  
- **/dashboard** → visualizaciones simples de tablas finales (golden)  
- **/reversion** → archivos para eliminar tablas lógicas y rutas físicas  
- **/.github/workflow** → despliegue de dev a prod  
- **/seguridad** → grants brindados a usuarios y grupos de tablas, schemas, etc.  
- **/PrepAmb** → creación de catalog, schemas, tablas, external locations, etc.  
- **/proceso** → notebooks de ETL  
- **/evidencias** → screenshots de los servicios de Azure y ejecuciones  
- **/readme.md** → explicación detallada del proyecto realizado

# 📁 Workflow Databricks
  <img width="954" height="426" alt="pipelineCompletado" src="https://github.com/user-attachments/assets/19a57d30-d827-44ad-b34a-8e569d0d645f" />

# 🚀 CI/CD

Para automatizar el despliegue entre los entornos de desarrollo y producción se utiliza **GitHub Actions**.

## Requisitos

Antes de ejecutar el pipeline es necesario configurar:

- Una credencial de GitHub.
- Cuatro *tokens* de autenticación (Secrets) en el repositorio.

Estos elementos permiten establecer una conexión segura entre el entorno de **Databricks Development** y **Databricks Production**, de manera que el proceso de despliegue pueda ejecutarse automáticamente.

GitHub ejecuta automáticamente un archivo de configuración **YAML** (`.yml`).

Este archivo contiene la definición del **workflow**, donde se especifican los pasos necesarios para realizar el despliegue, como la autenticación con Databricks, la validación del proyecto y la publicación en el entorno de producción.

## Flujo de despliegue

El proceso de CI/CD se realiza mediante **GitHub Actions**, el cual ejecuta el pipeline cada vez que ocurre el evento de pull request.

<p align="center">
  <img width="539" alt="GitHub Actions Pipeline" src="https://github.com/user-attachments/assets/b02532f6-c73b-4abf-a520-a7d4671870f8">
</p>


# 👤 Autor
### Marlon Josue Quiros Bosque

Proyecto: Data Engineering - Arquitectura Medallion
Tecnología: Azure Databricks + Delta Lake + CI/CD
