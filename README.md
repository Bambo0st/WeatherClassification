# Weather Classification 

This project focuses on classifying weather conditions using machine learning techniques, based on exploratory data analysis (EDA), preprocessing, and model optimization.

## Project Overview

This project is part of the AI-511 Machine Learning course, developed as an assignment at the International Institute of Information Technology Bangalore. The goal is to create an accurate weather classification model by exploring various machine learning algorithms and optimizing their hyperparameters.

**Team Members:**
- Achintya Harsha (IMT2021525)
- Adithya Nagaraja Somasalle (IMT2021054)
- Devendra Rishi Nelapati (IMT2021076)

## Table of Contents

1. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
2. [Data Preprocessing](#data-preprocessing)
3. [Model Training and Testing](#model-training-and-testing)
4. [Results](#results)

## Exploratory Data Analysis (EDA)

1. **Handling Null Values:** Columns with a high percentage of null values (e.g., Sunshine and Evaporation) were dropped due to their potential to degrade model accuracy.
2. **Feature Distribution:** Distribution of both numerical and categorical features was analyzed to remove low-variance features.
3. **Correlation Analysis:** Features with low correlation with the target variable were removed.
4. **Outlier Detection:** Boxplots were used to detect and remove outliers to improve data quality.

## Data Preprocessing

1. **Date Decomposition:** The date column was split into day, month, and year to simplify categorical values.
2. **Location-Based Probability Calculation:** A probability metric was computed for each location, indicating the likelihood of a specific weather task being true.
3. **Seasonal Categorization:** Data was divided by seasons, with imputation based on seasonal averages for missing values.
4. **Upsampling and Downsampling:** Imbalance in the target values was addressed by balancing class distributions through upsampling and downsampling.
5. **Encoding:** Label encoding was used for categorical data, achieving higher accuracy than one-hot encoding.

## Model Training and Testing

The following machine learning models were evaluated:
- **K-Nearest Neighbors (KNN)**
- **Logistic Regression**
- **LightGBM Classifier**
- **Random Forest Classifier**
- **AdaBoost Classifier**
- **XGBoost Classifier (Best Model)**

### XGBoost Model

The XGBoost model achieved the highest accuracy (68.13%) with optimal preprocessing and tuning:
- Initial accuracy: 64.40%
- Final accuracy after seasonal categorization and early stopping: 68.13%

## Results

XGBoost demonstrated the best performance on the dataset, surpassing other models through progressive improvements in data preprocessing and hyperparameter tuning.
