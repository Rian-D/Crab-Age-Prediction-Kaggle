# Crab Age Prediction
My machine learning solution for the Kaggle Crab Age Prediction competition, earning me an MAE of 1.404 (**top 10%** of all submissions). The source code as well as a more detailed analysis of my thought process when writing the code can be found in **main.ipynb**.

## Competition Overview
This project tackles the [Regression with a Crab Age Dataset Kaggle Competition](https://www.kaggle.com/competitions/playground-series-s3e16/overview). The goal is to predict the age of crabs based on physical measurements including dimensions and weight components.

**Evaluation Metric:** Mean Absolute Error (MAE)


## Dataset Summary
- **Training Data:** 74,051 crabs with age measurements
- **Test Data:** 49,368 crabs (predictions needed for submission) 
- **Features:** 8 variables including length, diameter, height, and various weight measurements
- **Target:** Age (continuous variable)


## Methodology

### 1. Exploratory Data Analysis (including data visualisation, correlation testing...)

### 2. Data Quality Assessment & Cleaning

### 2. Feature Engineering (transformed 5 existing features, derived 9 new features)

### 3. Feature Selection & Impact Testing

### 4. Data Preprocessing Pipelines (via imputation, scaling and one-hot-encoding)

### 5. Hyperparameter Optimisation (RandomizedSearchCV)

### 4. Model Training & Validation (XGBoost)


## License
This project is licensed under the MIT License.

*This project was developed as part of the Regression with a Crab Age Dataset Kaggle competition to demonstrate machine learning techniques for biological regression problems.*
