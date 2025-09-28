# Loan-Prediction-Project
Description:
A machine learning project to predict loan approval using customer demographic and financial data.

📖 Project Overview

  This project aims to build a predictive model to determine whether a loan will be approved or rejected based on customer and financial features. 
The workflow includes:

  Data preprocessing and handling missing values

  Exploratory data visualization

  Feature encoding and scaling

  Model building using Logistic Regression with balanced class weight

Evaluation on train and test sets using accuracy, confusion matrix, classification report, and ROC AUC

📂 Dataset

The dataset loan_data_set.csv contains the following columns:

| Column              | Description                                           |
| ------------------- | ----------------------------------------------------- |
| `Loan_ID`           | Unique loan identifier (dropped during preprocessing) |
| `Gender`            | Applicant’s gender                                    |
| `Married`           | Marital status                                        |
| `Dependents`        | Number of dependents                                  |
| `Education`         | Applicant’s education level                           |
| `Self_Employed`     | Employment type                                       |
| `ApplicantIncome`   | Applicant’s income                                    |
| `CoapplicantIncome` | Co-applicant’s income                                 |
| `LoanAmount`        | Loan amount requested                                 |
| `Loan_Amount_Term`  | Loan repayment term                                   |
| `Credit_History`    | Credit history (1 = good, 0 = bad)                    |
| `Property_Area`     | Area of property                                      |
| `Loan_Status`       | Target variable (1 = approved, 0 = rejected)          |

🛠️ Tools & Technologies

  Language: Python

  Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

  Machine Learning Model: Logistic Regression (class-weight balanced)

  Environment: Google Colab
  
🔹 Methodology

  Data Exploration & Visualization

  Analyzed distribution of loan status and missing values.

  Data Preprocessing

  Imputed missing values using median or mode.

  Encoded categorical features and the target variable.

  Scaled numerical features to standardize ranges.

  Model Training & Evaluation

  Split dataset into training and testing sets.

  Trained Logistic Regression with balanced class weights to handle class imbalance.

  Evaluated using accuracy, confusion matrix, classification report, and ROC AUC.

📊 Results

Model Performance:

| Dataset | Accuracy | ROC AUC | Observations                                                   |
| ------- | -------- | ------- | -------------------------------------------------------------- |
| Train   | 76.6%    | 0.718   | Balanced predictive power; high recall for approved loans      |
| Test    | 74.8%    | 0.699   | Model generalizes well; consistent performance with train data |

Key Insights:

Model predicts approved loans (class 1) very well.

Recall for rejected loans (class 0) is moderate but consistent.

Small difference between train and test metrics indicates no severe overfitting.

Random Forest

| Dataset | Accuracy | ROC AUC | Observations                                                       |
| ------- | -------- | ------- | ------------------------------------------------------------------ |
| Train   | 100%     | 1.0     | Perfect fit on training data (possible overfitting)                |
| Test    | 78.0%    | 0.702   | High recall for approved loans; moderate recall for rejected loans |

Key Insights:

Both models perform better on approved loans (class 1).

Recall for rejected loans (class 0) is moderate but consistent.

Logistic Regression generalizes better, while Random Forest shows perfect training accuracy but slightly lower test performance, indicating some overfitting.

🔮 Future Work

Feature engineering to improve prediction for rejected loans

Deploy as a web application for real-time loan approval prediction
