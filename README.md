# Task 1: Term Deposit Subscription Prediction

## 📌 Objective
The objective of this project is to predict whether a bank customer will subscribe to a term deposit as a result of a marketing campaign.

This is a binary classification problem where:
- 1 → Customer subscribed to term deposit
- 0 → Customer did not subscribe

---

## 📊 Dataset
- **Name:** Bank Marketing Dataset
- **Source:** UCI Machine Learning Repository / Kaggle
- **File Used:** bank-additional-full.csv
- **Target Variable:** y (Yes/No)

### Key Features:
- age → Customer age
- job → Occupation
- marital → Marital status
- education → Education level
- housing → Housing loan status
- loan → Personal loan status
- contact → Communication type
- campaign → Number of contacts during campaign
- duration → Duration of last contact
- economic indicators (e.g., euribor3m, emp.var.rate)

---

## 🛠 Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- SHAP (Explainable AI)

---

## 🔍 Project Workflow

### 1️⃣ Data Loading & Understanding
- Loaded dataset using Pandas
- Explored data using `.info()`, `.describe()`, and `.head()`

### 2️⃣ Data Preprocessing
- Converted target variable (yes/no → 1/0)
- Applied One-Hot Encoding to categorical variables
- Converted boolean values to numeric (0/1)
- Ensured dataset contains only numeric values

### 3️⃣ Exploratory Data Analysis (EDA)
- Analyzed age distribution
- Studied job-wise subscription patterns
- Analyzed impact of contact type on subscription

### Key Observations:
- Certain job categories have higher subscription rates
- Contact method significantly influences customer response
- Campaign-related features impact success rate

---

## 🤖 Model Building

### Models Used:
- Logistic Regression
- Random Forest Classifier

### Training:
- Split dataset into training (80%) and testing (20%)
- Trained both models and compared performance

---

## 📈 Model Evaluation

Evaluated using:
- Accuracy Score
- Confusion Matrix
- F1 Score
- ROC Curve (AUC)

### Results:
- Random Forest performed better than Logistic Regression
- Model shows good classification performance
- ROC curve indicates strong predictive capability

---

## 🔥 Explainable AI (SHAP)

- Used SHAP to interpret model predictions
- Generated:
  - SHAP summary (beeswarm) plot
  - Individual prediction explanations (waterfall plots)

### Insights from SHAP:
- Duration of contact is a major factor
- Economic indicators influence decisions
- Campaign-related features affect outcomes

---

## 🧠 Business Insights

- Customers contacted via cellular are more likely to subscribe
- Longer interaction duration increases conversion probability
- Targeting specific job categories can improve marketing success
- Campaign optimization can reduce costs and increase efficiency

---

## ✅ Conclusion

The Random Forest model successfully predicts customer subscription behavior with strong performance.

SHAP analysis provides transparency into model decisions, making the model more trustworthy and useful for real-world business applications.

This solution can help banks:
- Improve marketing strategies
- Target high-probability customers
- Optimize campaign performance

---

## 📂 Project Structure
Term_Deposit_Prediction/
│
├── term_deposit_prediction.ipynb
└── README.md

