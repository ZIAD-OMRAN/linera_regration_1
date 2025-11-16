Medical Charge Prediction using Linear Regression
Project Overview
This project aims to predict individual medical insurance charges using linear regression. The analysis is conducted in a Jupyter Notebook (linear_regration_1.ipynb) and involves exploratory data analysis (EDA), feature preprocessing, and model training using scikit-learn. The primary goal is to identify the key factors influencing medical costs and build a predictive model to estimate charges.

Dataset
The project uses the "Medical Charges" dataset, which contains 1338 rows of data on individual insurance beneficiaries.

Source: Medical Charges CSV on GitHub

Features
age: Age of the primary beneficiary.

sex: Gender (male, female).

bmi: Body mass index.

children: Number of children covered by health insurance.

smoker: Smoking status (yes, no).

region: The beneficiary's residential area in the US.

charges (Target): Individual medical costs billed by health insurance.

Project Workflow
Data Loading & Inspection: The dataset is loaded from the URL using pandas. Initial checks are performed using .info() and .describe() to understand data types, identify any missing values, and review statistical summaries.

Exploratory Data Analysis (EDA):

Visualized the distributions of age, bmi, and charges using histograms. The charges feature was noted to be positively skewed.

Analyzed the distributions of categorical features (sex, region, smoker) using count plots.

Used scatter plots to investigate the relationships between features and the target variable (charges).

Generated a correlation heatmap to quantify the linear relationships between numerical features.

Feature Preprocessing:

Categorical Features: sex, smoker, and region were converted to numerical values using sklearn.preprocessing.LabelEncoder.

Numerical Features: age, bmi, and children were scaled using sklearn.preprocessing.StandardScaler to normalize their range and ensure they contribute equally to the model.

Model Training:

The fully preprocessed dataset was split into training (90%) and testing (10%) sets.

A LinearRegression model from scikit-learn was trained on the training data.

Model Evaluation:

The trained model was used to make predictions on the test set.

Performance was measured using Root Mean Squared Error (RMSE) to determine the average error of the model's predictions.

Key Findings from EDA
Smoker status is the most significant predictor of medical charges. The scatter plots clearly show that smokers have substantially higher charges than non-smokers.

Age and BMI also show a strong positive correlation with charges.

The relationship between age and charges revealed three distinct clusters, which correspond to non-smokers, smokers, and smokers with a high BMI.

Model Performance
Model: Linear Regression

Test MSE (Mean Squared Error): 32,402,757.39

Test RMSE (Root Mean Squared Error): 5,692.34

Libraries Used
pandas

numpy

seaborn

matplotlib.pyplot

scikit-learn (for LinearRegression, train_test_split, mean_squared_error, LabelEncoder, StandardScaler)
