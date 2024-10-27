# Weather Classification Project

This project focuses on classifying weather conditions using machine learning techniques, specifically emphasizing data preprocessing and model optimization to enhance accuracy.

## Project Overview

This project is part of the AI-511 Machine Learning course at the International Institute of Information Technology Bangalore. The goal is to build a highly accurate weather classification model by experimenting with multiple machine learning models and refining preprocessing techniques.

**Team Members:**
- Achintya Harsha (IMT2021525)
- Adithya Nagaraja Somasalle (IMT2021054)
- Devendra Rishi Nelapati (IMT2021076)

## Table of Contents

1. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
2. [Data Preprocessing](#data-preprocessing)
3. [Model Training and Testing](#model-training-and-testing)
4. [XGBoost Accuracy Progression](#xgboost-accuracy-progression)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Conclusion](#conclusion)

## Exploratory Data Analysis (EDA)

1. **Handling Null Values:** Columns with a high percentage of null values (e.g., Sunshine and Evaporation) were dropped to avoid degrading model accuracy.
2. **Feature Distribution:** The spread of values in numerical and categorical features was analyzed, and low-variance features were removed.
3. **Correlation Analysis:** Features with low correlation to the target variable were excluded.
4. **Outlier Detection:** Outliers were identified and removed using boxplots, improving the quality of data.

## Data Preprocessing

1. **Date Decomposition:** The date column was split into day, month, and year, simplifying categorical values.
2. **Location-Based Probability Calculation:** A probability metric was calculated for each location to reflect the likelihood of specific weather conditions.
3. **Seasonal Categorization:** Data was categorized by season, and imputation was performed based on seasonal averages.
4. **Upsampling and Downsampling:** Class imbalance was addressed through upsampling and downsampling, balancing target values.
5. **Encoding:** Label encoding and categorical encoding were applied, with categorical encoding yielding higher accuracy.

## Model Training and Testing

The following machine learning models were evaluated:
- **K-Nearest Neighbors (KNN)**
- **Logistic Regression**
- **LightGBM Classifier**
- **Random Forest Classifier**
- **AdaBoost Classifier**
- **XGBoost Classifier (Best Model)**

## XGBoost Accuracy Progression

XGBoost demonstrated the highest performance on the dataset, with accuracy improvements as follows:

- **64.40%** - Basic XGBoost with minimal preprocessing and no hyperparameter tuning.
- **65.52%** - Improved by dropping columns with low correlation and variance.
- **66.82%** - Handled class imbalance through upsampling and downsampling.
- **67.18%** - Replaced label encoding with categorical encoding.
- **67.97%** - Implemented seasonal data categorization.
- **68.13%** - Applied early stopping in XGBoost to prevent overfitting.

## Results

XGBoost demonstrated the best performance on the dataset, surpassing other models through progressive improvements in data preprocessing and hyperparameter tuning.
