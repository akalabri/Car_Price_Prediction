# Used Car Price Prediction Project

## Overview

This project aims to develop and evaluate machine learning models to predict the price of used cars. The project is divided into three main steps: Data Preprocessing, Exploratory Data Analysis (EDA), and Model Development and Evaluation. Each step is documented in a separate Jupyter notebook, ensuring a structured and easy-to-follow workflow.

## Repository Structure

- `Data_Preprocessing.ipynb`: This notebook contains all the preprocessing steps, including handling missing values, encoding categorical features, and normalizing numerical features.
- `EDA.ipynb`: This notebook is dedicated to Exploratory Data Analysis, providing visualizations and insights into the dataset's feature distributions, correlations, and outliers.
- `ML-with Outliers.ipynb`: In this notebook, various machine learning models are developed and evaluated using the dataset with outliers that was created during EDA.
- `ML-No Outliers.ipynb`: This notebook repeats the machine learning workflow, but with a dataset where outliers have been removed from the target variable (price).

## Project Workflow

### 1. Data Preprocessing (`Data_Preprocessing.ipynb`)

In this initial step, the training and test datasets are loaded and cleaned. Specific tasks include handling missing values, converting data types, performing feature engineering, and applying one-hot encoding to categorical features. The preprocessed data is then saved to CSV files for future use.

### 2. Exploratory Data Analysis (EDA) (`EDA.ipynb`)

The EDA notebook starts by importing the preprocessed data. It focuses on visualizing the data to understand the distributions of different features, identify potential outliers, and explore relationships between features and the target variable (car prices). During outliers analysis, two seperate dataframes are created to then test if removing outliers would help the accuracy. 

### 3. Model Development and Evaluation with Outliers (`ML-with Outliers.ipynb`)

This notebook loads the preprocessed data and applies various regression models to predict car prices. The models are evaluated based on their performance metrics, and the results are visualized for interpretation. The models include Linear Regression, K-Nearest Neighbors Regression, Decision Tree Regression, and Gradient Boosting Regression.

### 4. Model Development and Evaluation without Outliers (`ML-No Outliers.ipynb`)

The workflow in this notebook is similar to the previous one, but it uses a version of the dataset where outliers in the price column have been removed. This aims to understand how the removal of outliers affects the performance of the machine learning models.

## Conclusion and Next Steps

This project provides a comprehensive approach to predicting used car prices, from data preprocessing and exploratory analysis to model development and evaluation. It was found that the decision tree model is the best model for this dataset using the metrices in this project. Additionally, removing the outliers did indeed decrease the MAE of the models significanlty but the models were poorly fitted which was indicated by an R-Squared value close to zero. Here is a comparison between the decision trees models for both datasets. Threfore, it was concluded that using the decsion tree model trained by the data wiht outliers is the best fit for this scinario. 
![Image 1](https://raw.githubusercontent.com/akalabri/Car_Price_Prediction/main/with_Outliers.png?token=GHSAT0AAAAAACIKBX2FDQAMJ5QOGQDH7OMSZJYXVBQ) ![Image 2](https://raw.githubusercontent.com/akalabri/Car_Price_Prediction/main/No_Outliers.png?token=GHSAT0AAAAAACIKBX2FE47Q5NXLIY7WXQ5IZJYXUYA)

Future work could include fine-tuning the models, experimenting with additional features, and deploying the models for real-time predictions. Also, adding a dashboard for the EDA section will be very helpful in delivering the results to the users. Moreover, building a webiste based interface to predict the car price given certain inputs will be very helpful as well
