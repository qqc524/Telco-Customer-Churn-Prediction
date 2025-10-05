# 📊 Telco Customer Churn Prediction

## 📖 Project Overview

This project explores why customers leave a telecommunications company (known as **customer churn**) and how machine learning can help predict it.  
Customer churn is a major problem because keeping current customers is usually cheaper than getting new ones.

The dataset, provided by IBM, contains information about **7,043 customers** of a fictional telecom company in California.  

This project aims to help companies:

- Understand what drives churn  
- Improve customer retention strategies  
- Offer better services and targeted promotions  


## 🧩 Project Steps

### 1. Exploratory Data Analysis (EDA) & Cleaning
- Checked for missing data and fixed data type issues  
- Cleaned categorical and numeric features  
- Created a new cleaned dataset for modeling  

📁 See **EDA & Data Cleaning notebook** for detailed exploration steps.



### 2. Modeling and Evaluation
This notebook focuses on building and comparing several **tree-based machine learning models** using the cleaned dataset.

#### Models Used
- Decision Tree  
- Random Forest  
- XGBoost  
- LightGBM  

These models were chosen because they:
- Handle categorical variables effectively  
- Capture non-linear patterns in customer behavior  
- Are robust to outliers and unscaled data  
- Provide insights into **feature importance**


## ⚙️ Data Preparation
- **Target variable:** `Churn` (Yes/No)  
- **Features:** Demographics, service types, contract info, payment method, tenure, and charges  
- **Preprocessing:**  
  - One-hot encoding for categorical columns  
  - Numeric features kept unchanged  
- **Train-Test Split:** 80% training, 20% testing  


## 🧠 Model Evaluation

Each model was evaluated using:
- **Accuracy** – Overall correctness  
- **Precision** – Correctly predicted churns  
- **Recall** – How many churns were caught  
- **F1-Score** – Balance between precision and recall  
- **ROC-AUC** – Ability to separate churn vs non-churn customers  

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|:--|:--:|:--:|:--:|:--:|:--:|
| Decision Tree | 0.72 | 0.48 | 0.50 | 0.49 | 0.65 |
| Random Forest | 0.79 | 0.63 | 0.49 | 0.55 | 0.82 |
| XGBoost | 0.78 | 0.61 | 0.51 | 0.55 | 0.82 |
| **LightGBM** | **0.79** | **0.62** | **0.53** | **0.57** | **0.84** |


## 🔍 Findings
- **LightGBM** performed the best overall:
  - Highest accuracy (79%)
  - Best recall (53%)
  - Strong ROC-AUC (0.84)
- **Decision Tree** performed the weakest due to overfitting.
- **Ensemble models** (Random Forest, XGBoost, LightGBM) produced better and more stable results.


## ✅ Conclusion
The **LightGBM model** is the most reliable for predicting customer churn.  
It achieves a strong balance between accuracy, recall, and ROC-AUC - making it ideal for identifying customers likely to leave.



## 🧰 Tools and Libraries
- Python  
- Pandas, NumPy, Matplotlib, Scikit-learn  
- XGBoost, LightGBM  
- Jupyter Notebook  
