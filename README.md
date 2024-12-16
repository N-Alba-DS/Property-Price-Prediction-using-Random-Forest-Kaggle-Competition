# Predicción de Precios de Propiedades en Buenos Aires utilizando Random Forest
Este repositorio contiene el código y la documentación del proyecto de predicción de precios de propiedades en la Ciudad Autónoma de Buenos Aires, desarrollado como trabajo final para la competencia de Kaggle organizada por la materia de Data Mining de la “Maestría en Explotación de Datos y Descubrimiento del Conocimiento” de la UBA.

[Competencia de Kaggle - Predicción de Precio de Propiedades](https://www.kaggle.com/competitions/fcen-dm-2024-prediccion-precio-de-propiedades/overview)
## Descripción del Trabajo

Este proyecto aplica técnicas de minería de datos impartidas en la materia Data Mining del primer semestre de la **Maestría en Explotación de Datos y Descubrimiento del Conocimiento** de la UBA. El objetivo es predecir los valores de propiedades en la Ciudad Autónoma de Buenos Aires.

La estrategia general consistió en entrenar modelos de regresión segmentados por subgrupos de propiedades, realizando una segmentación jerárquica del conjunto de datos. Estos subgrupos buscan encontrar modelos que reduzcan el sesgo y sean capaces de capturar la máxima varianza sin sobreajustar, con el fin de minimizar la **Raíz del Error Cuadrático Medio (RMSE)**, la métrica utilizada en la competencia para evaluar las predicciones.

Se desarrollaron cuatro modelos, cada uno enfocado en un tipo diferente de propiedad:

- **Departamentos**
- **Departamentos en Puerto Madero**
- **Casas**
- **Cocheras**
## Librerías Utilizadas

El script fue desarrollado en Python y utiliza las siguientes librerías principales:

- **Pandas** y **NumPy**: Para tareas de ETL (Extracción, Transformación y Carga) y manipulación de datos.
- **Matplotlib** y **Plotly**: Para la visualización de datos.
- **Scikit-learn**:
  - `RandomForestRegressor`: Como modelo de predicción.
  - `GridSearchCV`: Para la optimización de hiperparámetros.
  - `KFold`: Para la validación cruzada.

## Técnicas Utilizadas

- **Preprocesamiento y Manipulación de Datos**:
  - Limpieza y preparación de datos con Pandas.
  - Concatenación de diferentes modelos y conjuntos de datos.

- **Codificación de Variables Categóricas**:
  - **One-Hot Encoding**.
  - **Ordinal Encoding**.

- **Procesamiento de Texto**:
  - Extracción de información mediante expresiones regulares (Regex).

- **Detección y Tratamiento de Valores Atípicos (Outliers)**:
  - Análisis univariado y multivariado para identificar outliers.
  - Aplicación de técnicas para su tratamiento.

- **Imputación de Datos Faltantes**:
  - Utilización de algoritmos de imputación multivariada como **MICE**.
  - Imputación basada en **KNN**.

- **Ingeniería de Características (Feature Engineering)**:
  - Creación de nuevas variables relevantes.
  - Transformación y reescalado de la variable objetivo (target).

- **Validación y Optimización del Modelo**:
  - Validación cruzada con **KFold**.
  - Búsqueda de hiperparámetros óptimos con **GridSearchCV**.



## Conclusiones

- La segmentación por tipo de propiedad (Casas, departamentos y cocheras) y jerárquica (entre departamentos de Puerto Madero y el resto de CABA), permitió reducir el sesgo y mejorar la precisión de las predicciones.
- El uso de técnicas de imputación avanzadas (MICE y KNN) contribuyó a manejar eficazmente los datos faltantes.
- La optimización de hiperparámetros mediante GridSearchCV y la validación cruzada fueron fundamentales para evitar el sobreajuste. Remarcando que debido a la inexperiencia al momento del proyecto no se contaba con conocimientos de otras herramientas más eficientes de optimización que implementaran optimización bayesiana. 
