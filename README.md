# 📞 Telco Customer Churn Analysis

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-brightgreen)
![Matplotlib](https://img.shields.io/badge/Visualization-Matplotlib-orange)
![License](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)

---

## 🚀 Project Overview
This project analyzes **customer churn** for a telecommunications company using real-world data on demographics, contracts, services, and billing.  
The goal is to identify which customers are at risk of leaving and why, enabling **data-driven retention strategies**.

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
   - Handle missing values and blanks.  
   - Convert `TotalCharges` to numeric and impute missing values.  
   - Remove duplicates.  
   - Encode target variable `Churn`.  

2. **Exploratory Data Analysis (EDA)**
   - Numeric features: `tenure`, `MonthlyCharges`, `TotalCharges`.  
   - Categorical features: `gender`, `InternetService`, `Contract`, `PaymentMethod`.  

3. **Feature Engineering**
   - Create **tenure groups** and **total services**.  
   - Calculate **average charge per service**.  

4. **Correlation & Risk Analysis**
   - Identify groups linked to high churn using correlation heatmaps.  

5. **Business Insights & Recommendations**
   - Reduce churn via **onboarding**, **bundles**, and **contract upgrades**.

---

## 🏆 Key Findings

- ![High Churn](https://img.shields.io/badge/Month-to-Month_High_Churn-red) Churn is highest among **month-to-month contracts**.  
- ![Fiber Optic](https://img.shields.io/badge/Fiber_Optic_High_Churn-orange) **Fiber optic internet users** have higher churn.  
- ![New Customers](https://img.shields.io/badge/New_Customers_High_Risk-yellow) **New customers** are more likely to leave.  
- ![Bundling](https://img.shields.io/badge/Service_Bundles_Lower_Churn-green) Customers with **more bundled services** are less likely to churn.  
- Retention strategies should focus on **onboarding, bundling, and contract upgrades**.

---

## 📈 Visualizations

### Numeric Features
| Feature | Histogram | Boxplot |
|---------|-----------|---------|
| Tenure | ![Tenure Histogram]<img width="800" height="400" alt="tenure_histogram" src="https://github.com/user-attachments/assets/5b06c33c-c86e-4d94-911f-f001c5bd06b5" /> | ![Tenure Boxplot] <img width="800" height="400" alt="tenure_boxplot" src="https://github.com/user-attachments/assets/8faf1849-09a1-46bd-bf21-d88303c48962" />
|
| Monthly Charges | ![MonthlyCharges Histogram]<img width="800" height="400" alt="MonthlyCharges_histogram" src="https://github.com/user-attachments/assets/8a056cff-1774-4367-8c68-60bec74ba48e" /> | ![MonthlyCharges Boxplot] <img width="800" height="400" alt="MonthlyCharges_boxplot" src="https://github.com/user-attachments/assets/2dc27c07-1bb9-472c-ac2b-8b41bce31d49" />
|
| Total Charges | ![TotalCharges Histogram]<img width="800" height="400" alt="MonthlyCharges_histogram" src="https://github.com/user-attachments/assets/be601f0e-55b1-46b1-b885-d56b294f6961" /> | ![TotalCharges Boxplot]<img width="800" height="400" alt="TotalCharges_boxplot" src="https://github.com/user-attachments/assets/aecb1f5e-b668-4a9b-8849-657e9a49fa25" />|

### Categorical Features
| Feature | Countplot | Churn Rate |
|---------|-----------|------------|
| Gender | ![Gender Countplot](images/gender_countplot.png) | ![Gender Churn Rate](images/gender_churn_rate.png) |
| Internet Service | ![InternetService Countplot](images/InternetService_countplot.png) | ![InternetService Churn Rate](images/InternetService_churn_rate.png) |
| Contract | ![Contract Countplot](images/Contract_countplot.png) | ![Contract Churn Rate](images/Contract_churn_rate.png) |
| Payment Method | ![PaymentMethod Countplot](images/PaymentMethod_countplot.png) | ![PaymentMethod Churn Rate](images/PaymentMethod_churn_rate.png) |

### Correlation Heatmap
![Correlation Heatmap](images/correlation_heatmap.png)

---

## 📝 How to Use
- Open `churn_analysis.ipynb` or `.py` for the full workflow.  
- All charts are saved in the `/images/` folder for GitHub embedding.

---

## 📂 Dataset
- `WA_Fn-UseC_-Telco-Customer-Churn.csv`  
  *(Please respect dataset license/source.)*

---

## 💡 Business Impact
The analysis identifies the **strongest drivers of churn**, enabling telecom companies to:  
- Improve **customer retention** via targeted onboarding.  
- Promote **bundled services** to reduce churn risk.  
- Encourage **contract upgrades** for long-term loyalty.  

This helps companies **retain customers longer** and optimize revenue.
