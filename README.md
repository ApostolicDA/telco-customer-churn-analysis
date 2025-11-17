# 📞 Telco Customer Churn Analysis

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-brightgreen)
![Matplotlib](https://img.shields.io/badge/Visualization-Matplotlib-orange)
![License](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)

---

## 🚀 Project Overview
In this **Customer churn analysis** for a telecommunications company using data on demographics, contracts, services, and billing.We identified which customers are at **risk of leaving** and why,enabling **data-driven retention strategies.**
---

## 📊 Project Summary

| Aspect | Description |
|--------|-------------|
| **Dataset** | `WA_Fn-UseC_-Telco-Customer-Churn.csv` |
| **Rows & Columns** | ~7,000 rows, 21 columns |
| **Target Variable** | `Churn` (0 = No, 1 = Yes) |
| **Key Features** | `tenure`, `MonthlyCharges`, `TotalCharges`, `Contract`, `InternetService`, `PaymentMethod`, `gender` |
| **Visualizations** | Histograms, boxplots, countplots, churn rate bars, correlation heatmap |
| **Output** | Plots saved in `/images/` folder for GitHub embedding |
| **Business Focus** | Improve retention via onboarding, bundling, and contract upgrades |

---

## 🛠 Project Steps

1. **Data Cleaning**
   - Handle missing values.  
   - Convert `TotalCharges` to numeric and impute missing values.  
   - Remove duplicates.  
   - Encode target variable `Churn`.  

2. **Exploratory Data Analysis (EDA)**
   - Numeric features: `tenure`, `MonthlyCharges`, `TotalCharges`.  
   - Categorical features: `gender`, `InternetService`, `Contract`, `PaymentMethod`.  

3. **Feature Engineering**
   - Create tenure groups and service counts.  
   - Compute average charge per service.  

4. **Correlation & Risk Analysis**
   - Use correlation heatmaps and category performance analysis.  

5. **Business Insights**
   - Focus on onboarding, service bundles, and contract upgrades.

---

## 🏆 Key Findings

- Churn is highest among **month-to-month contract customers**.  
- **Fiber optic users** churn more.  
- Customers with **short tenure** are more likely to leave.  
- Customers with **multiple bundled services** churn less.  

---

## 📈 Visualizations

### 📌 Numeric Features

| Feature | Histogram | Boxplot |
|--------|-----------|---------|
| **Tenure** | <img width="400" src="https://github.com/user-attachments/assets/5b06c33c-c86e-4d94-911f-f001c5bd06b5" /> | <img width="400" src="https://github.com/user-attachments/assets/8faf1849-09a1-46bd-bf21-d88303c48962" /> |
| **Monthly Charges** | <img width="400" src="https://github.com/user-attachments/assets/8a056cff-1774-4367-8c68-60bec74ba48e" /> | <img width="400" src="https://github.com/user-attachments/assets/2dc27c07-1bb9-472c-ac2b-8b41bce31d49" /> |
| **Total Charges** | <img width="400" src="https://github.com/user-attachments/assets/be601f0e-55b1-46b1-b885-d56b294f6961" /> | <img width="400" src="https://github.com/user-attachments/assets/aecb1f5e-b668-4a9b-8849-657e9a49fa25" /> |

---

### 📌 Categorical Features

| Feature | Countplot | Churn Rate |
|--------|-----------|------------|
| **Gender** | <img width="400" src="https://github.com/user-attachments/assets/e1a65496-0c6c-4019-8d71-61fb44735379" /> | <img width="400" src="https://github.com/user-attachments/assets/04f767ab-28c9-4074-a6fb-4e4c0e5ff9a3" /> |
| **Internet Service** | <img width="400" src="https://github.com/user-attachments/assets/e04dd20c-a2da-4886-bd92-d11b0cda3c19" /> | <img width="400" src="https://github.com/user-attachments/assets/b54e2704-bcc1-41cf-8b86-eee1e444fb05" /> |
| **Contract Type** | <img width="400" src="https://github.com/user-attachments/assets/99c71ff5-356b-4292-8d8d-e4b280953dde" /> | <img width="400" src="https://github.com/user-attachments/assets/a73130ea-cadb-4f78-920c-58200e15a382" /> |
| **Payment Method** | <img width="400" src="https://github.com/user-attachments/assets/44abd2ba-f31a-4f70-8ffc-7671c9608c50" /> | <img width="400" src="https://github.com/user-attachments/assets/744eb583-d68a-438e-8453-2b3521fe9a38" /> |

---

### 🔥 Correlation Heatmap

| Heatmap |
|---------|
| <img width="700" src="https://github.com/user-attachments/assets/8d6f38a4-cf5a-47d5-b78d-6da3d5b5c92e" /> |

---

## 📝 How to Use
- Open the Jupyter Notebook or Python script to follow the full analysis workflow.  
- All plotted images are stored in `/images/` for use in documentation.

---

## 🐍 Example Python Code

```python
import pandas as pd
import numpy as np

# Load dataset
df = pd.read_csv(r"C:\Users\Downloads\WA_Fn-UseC_-Telco-Customer-Churn.csv")

# Replace blank strings with NaN
df.replace(r'^\s*$', np.nan, regex=True, inplace=True)

# Convert TotalCharges to numeric
df['TotalCharges'] = pd.to_numeric(df['TotalCharges'], errors='coerce')

# Fill missing values
for col in df.columns:
    if df[col].isnull().sum() > 0:
        if df[col].dtype in ['float64', 'int64']:
            df[col].fillna(df[col].median(), inplace=True)
        else:
            df[col].fillna(df[col].mode()[0], inplace=True)

# Encode target variable
df['Churn'] = df['Churn'].map({'No':0, 'Yes':1})

# Quick overview
print(df.shape)
print(df['Churn'].value_counts())


