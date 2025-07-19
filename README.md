# 📊 Credit Risk Analysis using Machine Learning

## 📄 Overview
This project aims to build a predictive model that identifies whether a loan applicant is likely to default (high-risk) or repay (low-risk) based on structured financial data. The workflow includes data preprocessing, class imbalance handling, model training, and performance evaluation.

---

## 📁 Dataset
- **Records**: 1000
- **Features Used**:
  - `credit_score`
  - `loan_amount`
  - `income`
  - `employment_length`
  - `debt_to_income`
- **Target Variable**: `loan_status`
  - `0` = Low Risk (likely to repay)
  - `1` = High Risk (likely to default)

---

## ⚙️ Methods Used
- **Data Preprocessing**
  - Checked for missing values (none found)
  - Scaled features using `StandardScaler`
    
- **Exploratory Data Analysis**
 
 - Target class distribution visualization
<img width="293" height="194" alt="Loan_Status_Distribution" src="https://github.com/user-attachments/assets/3b68d004-8fc2-4402-b587-c046ead2514c" />

  - Correlation heatmap
<img width="523" height="331" alt="Correlation_heatmap" src="https://github.com/user-attachments/assets/d5d43683-3cb4-4e4d-ab8d-dcc20ad08192" />

- Identified a significant **class imbalance** (≈3:1 in favor of high-risk loans).

- **Modeling Techniques**
  - Logistic Regression
  - Logistic Regression with `class_weight='balanced'`
  - Random Forest with `class_weight='balanced'`
- **Model Evaluation**
  - Accuracy
  - Precision, Recall, F1-score
  - Confusion Matrix

---

## 📊 Results

| Model                     | Accuracy | Recall (Low Risk) | Recall (High Risk) |
|--------------------------|----------|-------------------|--------------------|
| Logistic Regression       | 0.74     | 0.00              | 1.00               |
| Logistic (Balanced)       | 0.49     | 0.46              | 0.50               |
| Random Forest (Balanced)  | 0.72     | 0.08              | 0.95               |

 🟡 **Observation**:  
- The baseline model failed to predict low-risk loans due to imbalance.
- Class balancing improved fairness but lowered overall accuracy.  
- Random Forest handled imbalance better, achieving high recall for risky loans.

---

## 💡 Insights
- **Data imbalance** significantly impacts model reliability and fairness.
- Logistic Regression needs balancing strategies to function well on skewed datasets.
- **Random Forest** offers better performance in identifying risky borrowers.
- Evaluating with **recall and precision** (not just accuracy) is essential for real-world credit risk applications.

---- 

## 📦 Requirements
- Libraries:
  - pandas
  - numpy
  - scikit-learn
  - seaborn
  - matplotlib

----

**## 👤 Contacts**

Email: (7mishragaurav@gmail.com)
LinkedIn: (www.linkedin.com/in/gaurav-mishra-3788ba271)
Github: (https://github.com/mishragaurav7)

----
