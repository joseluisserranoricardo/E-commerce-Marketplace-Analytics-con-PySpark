# E-commerce Marketplace Analytics con PySpark

## Descripción del Proyecto

Este proyecto analiza un dataset real de e-commerce brasileño utilizando Apache Spark y Spark SQL.

El objetivo principal es explorar:
- desempeño de vendedores,
- comportamiento de clientes,
- eficiencia logística,
- tendencias de ventas,
- impacto de retrasos en la satisfacción del cliente.

El proyecto simula un flujo de trabajo típico de análisis y procesamiento de datos utilizado en entornos de Big Data y Data Engineering.

---

# Objetivos de Negocio

Este análisis busca responder las siguientes preguntas:

- ¿Qué categorías generan más ingresos?
- ¿Qué estados concentran el mayor volumen de ventas?
- ¿Cómo afectan los retrasos a la satisfacción del cliente?
- ¿Cómo evolucionan las ventas a lo largo del tiempo?
- ¿Qué vendedores tienen mejor desempeño?

---

# Dataset

Dataset utilizado:

[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

El dataset contiene información sobre:
- clientes,
- órdenes,
- productos,
- vendedores,
- pagos,
- reviews,
- logística y entregas.

---

# Tecnologías Utilizadas

- Apache Spark
- PySpark
- Spark SQL
- Python
- Matplotlib
- Google Colab
- Parquet
- GitHub

---

# Pipeline ETL

El proyecto sigue un flujo ETL completo:

## Extract
Carga de múltiples datasets CSV en DataFrames de Spark.

## Transform
Transformaciones realizadas:
- joins entre múltiples tablas,
- manejo de valores nulos,
- feature engineering,
- agregaciones,
- window functions,
- métricas de entrega,
- cálculo de revenue.

## Load
Exportación de datasets procesados en formato Parquet para almacenamiento eficiente y futuras tareas analíticas.

---

# Conceptos de Spark Implementados

El proyecto utiliza varios conceptos importantes de Spark:

- Spark SQL
- DataFrame API
- joins
- aggregations
- broadcast joins
- window functions
- cache/persist
- almacenamiento Parquet
- feature engineering
- lazy evaluation
- execution plans

---

# Tabla Analítica Principal

Se construyó una tabla analítica central mediante joins entre:
- orders,
- customers,
- order_items,
- products,
- sellers,
- payments,
- reviews.

Esta tabla sirvió como base para todos los análisis posteriores.

---

# Principales Insights

## Impacto de Retrasos en la Satisfacción del Cliente

<img width="557" height="406" alt="impacto de retrasos" src="https://github.com/user-attachments/assets/d8b875c5-d776-4c55-94b2-a61489ef751d" />

Las entregas tardías reciben calificaciones significativamente menores que las entregas a tiempo.

### Impacto de Retrasos en Reviews

Promedio de reviews:
- On Time: ~4.1
- Late: ~2.3

Esto sugiere que el desempeño logístico impacta directamente la satisfacción del cliente.

---

# Revenue por Categoría

Algunas categorías dominan claramente el revenue del marketplace.

### Top Categorías por Revenue

<img width="1049" height="603" alt="top categ por revenue" src="https://github.com/user-attachments/assets/583964c7-7add-4104-9f21-6d656cabccfd" />


Las categorías con mayores ingresos incluyen:
- cama_mesa_banho,
- beleza_saude,
- informatica_acessorios.

---

# Ventas por Estado

Las ventas están fuertemente concentradas en ciertos estados de Brasil.

### Top Estados por Ventas

<img width="862" height="499" alt="top estados" src="https://github.com/user-attachments/assets/baf1dc63-37ed-4b00-a5ff-d0a04906864c" />

São Paulo (SP) lidera ampliamente el volumen total de ventas.

---

# Tendencia Temporal de Ventas

El marketplace mostró un crecimiento importante durante 2017 y 2018.

### Ventas Mensuales

<img width="1034" height="526" alt="ventas mensuales" src="https://github.com/user-attachments/assets/013e86ff-9bfa-4910-9d82-db12493a7efa" />

El análisis muestra:
- crecimiento sostenido del revenue,
- fluctuaciones estacionales,
- picos de ventas entre finales de 2017 e inicios de 2018.

---

# Resultados del Proyecto

El proyecto permitió:
- integrar múltiples fuentes de datos,
- construir pipelines ETL con Spark,
- aplicar análisis analítico sobre datos reales,
- generar métricas de negocio relevantes,
- utilizar procesamiento distribuido con PySpark.

---

# Posibles Mejoras Futuras

Este proyecto puede extenderse con:
- dashboards interactivos,
- pipelines en tiempo real,
- modelos de machine learning,
- segmentación de clientes,
- sistemas de recomendación,
- despliegue en cloud,
- integración con Delta Lake.

---

# Conclusión

Este proyecto demuestra cómo Spark puede utilizarse para construir pipelines analíticos escalables sobre datos de e-commerce.

El análisis combina:
- ETL,
- procesamiento distribuido,
- analytics,
- visualización,
- optimización básica en Spark.

Además, el proyecto evidencia cómo la logística y el desempeño de entregas impactan directamente la experiencia del cliente y el rendimiento del marketplace.
