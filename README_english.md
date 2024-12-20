# Property Price Prediction in Buenos Aires using Random Forest

This repository contains the code and documentation for the property price prediction project in the Autonomous City of Buenos Aires, developed as a final assignment for the Kaggle competition organized by the Data Mining course of the **"Maestría en Explotación de Datos y Descubrimiento del Conocimiento"** (Master’s in Data Mining and Knowledge Discovery), Universidad de Buenos Aires (UBA).

[Kaggle Competition - Property Price Prediction](https://www.kaggle.com/competitions/fcen-dm-2024-prediccion-precio-de-propiedades/overview)

## Work Description

This project applies data mining techniques taught in the Data Mining course during the first semester of the Master’s in Data Mining and Knowledge Discovery at UBA. The goal is to predict property values in the Autonomous City of Buenos Aires.

The general strategy consisted of training regression models segmented by property subgroups, performing a hierarchical segmentation of the dataset. These subgroups aim to find models that reduce bias and are capable of capturing maximum variance without overfitting, in order to minimize the **Root Mean Squared Error (RMSE)**, the metric used in the competition to evaluate predictions.

Four models were developed, each focused on a different type of property:

- **Apartments**
- **Apartments in Puerto Madero**
- **Houses**
- **Parking Spaces (Cocheras)**

## Libraries Used

The script was developed in Python and uses the following main libraries:

- **Pandas** and **NumPy**: For ETL (Extraction, Transformation, and Loading) tasks and data manipulation.
- **Matplotlib** and **Plotly**: For data visualization.
- **Scikit-learn**:
  - `RandomForestRegressor`: As the prediction model.
  - `GridSearchCV`: For hyperparameter optimization.
  - `KFold`: For cross-validation.

## Techniques Used

- **Data Preprocessing and Manipulation**:
  - Data cleaning and preparation with Pandas.
  - Concatenation of different models and datasets.

- **Categorical Variable Encoding**:
  - **One-Hot Encoding**.
  - **Ordinal Encoding**.

- **Text Processing**:
  - Information extraction using regular expressions (Regex).

- **Outlier Detection and Treatment**:
  - Univariate and multivariate analysis to identify outliers.
  - Application of techniques for their treatment.

- **Missing Data Imputation**:
  - Use of multivariate imputation algorithms like **MICE**.
  - KNN-based imputation.

- **Feature Engineering**:
  - Creation of new relevant variables.
  - Transformation and rescaling of the target variable.

- **Model Validation and Optimization**:
  - Cross-validation with **KFold**.
  - Search for optimal hyperparameters with **GridSearchCV**.

## Conclusions

- Segmenting by property type (houses, apartments, and parking spaces) and hierarchically (between Puerto Madero apartments and the rest of CABA) helped reduce bias and improve prediction accuracy.
- The use of advanced imputation techniques contributed to effectively handling missing data.
- Hyperparameter optimization through GridSearchCV and cross-validation was fundamental to avoid overfitting. Highlighting that due to inexperience at the time of the project, there was no knowledge of other more efficient Bayesian optimization tools.

