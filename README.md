🏥 Medical Charge Prediction Project
📝 Overview
This project aims to analyze the factors influencing individual medical insurance charges and builds a linear regression model to predict these costs based on beneficiary attributes.

📊 Dataset
The project uses the "Medical Charges" dataset, which is publicly available and contains 1338 records.

Data Source: Medical Charges CSV

Features:
age: Age of the beneficiary.

sex: Gender (male/female).

bmi: Body Mass Index.

children: Number of children.

smoker: Smoking status (yes/no).

region: Geographical region of the beneficiary.

charges (Target): The medical costs.

🚀 Workflow
The project followed five key stages:

1. Data Loading and Inspection
Data was loaded using pandas.

Initial inspection was performed using .info() and .describe() to understand data types, check for missing values, and get an initial statistical summary.

2. Exploratory Data Analysis (EDA)
A visual analysis was conducted to understand patterns and relationships:

Distributions: Histograms were plotted to understand the distribution of age, bmi, and charges.

Categorical Analysis: countplot was used to show the distribution of sex, region, and smoker.

Key Relationships:

Scatter plots were used to examine the relationship between age vs. charges and bmi vs. charges, with color-coding based on smoker status.

A correlation heatmap was generated for all numerical features.

3. Preprocessing
To prepare the data for modeling, the following steps were taken:

Encoding: Categorical columns (sex, smoker, region) were converted to numerical values using LabelEncoder.

Scaling: Numerical features (age, bmi, children) were normalized using StandardScaler to ensure each feature contributed fairly to the model.

4. Modeling
The data was split into features (X) and the target variable (y).

The dataset was divided into training (90%) and testing (10%) sets using train_test_split.

A LinearRegression model from scikit-learn was trained on the training data.

5. Evaluation
The model's performance was evaluated on the test set using:

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

💡 Key Insights from EDA
Smoker: This is by far the most significant predictor of medical charges.

Age & BMI: Both show a strong positive correlation with charges. As age or BMI increases, the expected charges also increase.

Charge Distribution: The charges variable is positively skewed, indicating that most individuals have low medical costs, while a few have very high costs.

📈 Final Model Performance
The model produced the following results on the test data:

Mean Squared Error (MSE): 32,402,757.39

Root Mean Squared Error (RMSE): 5,692.34

This indicates that the model's predictions are, on average, off by approximately $5,692.

🛠️ Tools and Libraries Used
Python 3

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn
seaborn

matplotlib.pyplot

scikit-learn (for LinearRegression, train_test_split, mean_squared_error, LabelEncoder, StandardScaler)
