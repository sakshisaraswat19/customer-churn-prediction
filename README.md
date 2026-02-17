# Customer-churn-prediction
Customer churn refers to the phenomenon where customers stop using a company’s product or service. For subscription-based businesses, predicting churn is crucial because retaining existing customers is significantly cheaper than acquiring new ones.
In this project, the goal is to predict whether a customer is likely to churn or not based on their demographic details, account information, and service usage patterns using machine learning techniques.

This project focuses not only on building a predictive model but also on:
- Proper preprocessing of categorical data
- Handling class imbalance
- Using pipelines for production-ready workflows
= Interpreting results from a business perspective

# Problem Statement
Given historical customer data, build a machine learning model that can:
- Predict whether a customer will Churn (Yes/No)
- Handle imbalanced data
- Provide insights that help businesses take preventive actions such as targeted offers or retention strategies


# Dataset Description
The dataset contains customer-level information including:

# 1. Customer Demographics
- Gender
- Senior Citizen
- Partner
- Dependents

# 2. Account Information
- Tenure
- Contract Type
- Payment Method
- Paperless Billing

# 3. Services Used
- Phone Service
- Internet Service
- Online Security
- Streaming Services
- Tech Support

# 4. Target Variable
- Churn (1 = Yes, 0 = No)

# Exploratory Data Analysis (EDA)
Key steps performed during EDA:

- Checked class imbalance between churned and non-churned customers
- Analyzed tenure and monthly charges distribution
- Compared churn rates across:
- Contract types
- Payment methods
- Internet services
- Visualized numerical features using histograms with mean and median
Insight: Customers with month-to-month contracts and higher monthly charges show significantly higher churn rates.

# Data Preprocessing
# 1. Feature Selection
- Dropped customerID as it is a unique identifier and provides no predictive value.

# 2️. Handling Data Types
- Converted TotalCharges from object to numeric.
- Handled missing or blank values appropriately.

# 3️. Encoding Categorical Variables
- Nominal features → OneHotEncoder
- Ordinal features (Contract type) → OrdinalEncoder
- Used ColumnTransformer to apply different preprocessing steps to different columns.

  This ensured:
  - No artificial ordering for nominal variables
  - Clean, scalable preprocessing

# Handling Class Imbalance
Customer churn data is naturally imbalanced.
Techniques explored:
- SMOTE (Synthetic Minority Oversampling Technique)
- Class weight balancing
Important Note:
Accuracy alone is misleading in imbalanced datasets. More emphasis was placed on Recall and F1-score for churn class.

# Model Building
The following models were trained and evaluated:

- Logistic Regression
- Random Forest Classifier
- Decision Tree

# Model Evaluation
Evaluation metrics used:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

Key Results
- Accuracy ≈ 82%
- Recall (Churn class) ≈ 57%

Interpretation:
While accuracy is moderate, the model is able to correctly identify a significant portion of churners, which is more valuable from a business standpoint.

# Business Impact
This churn prediction model can help businesses:
- Identify customers at high risk of leaving
- Design targeted retention strategies
- Reduce revenue loss
- Improve customer lifetime value (CLV)
Even a small improvement in churn prediction can lead to significant cost savings.

# Tech Stack Used
- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)

# Future Improvements
- Feature engineering (e.g., average spend per tenure)
- Hyperparameter tuning
- Threshold tuning to improve churn recall
- Deploying the model as a web API

# Key Learnings
- Accuracy alone is not sufficient for imbalanced problems
- Proper encoding strategy is critical
- Pipelines are essential for clean and safe ML workflows
- Business understanding is as important as model performance

# Conclusion
This project demonstrates an end-to-end machine learning workflow for a real-world business problem. It balances technical rigor with practical business insights and is designed to be both interview-ready and production-ready.
