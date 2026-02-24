# Customer Churn Prediction & Analysis 📊

## 🎯 Project Objective
[cite_start]To predict whether a customer is likely to stop using a service (churn) based on behavioral, demographic, and service-related factors[cite: 5]. [cite_start]The ultimate goal of this project is to understand how companies can retain customers by identifying high-risk segments[cite: 10].

## 📁 Dataset Overview
[cite_start]This analysis utilizes the standard **Telco Customer Churn** dataset (often used in telecom, SaaS, and e-commerce contexts)[cite: 6, 12]. 
* [cite_start]**Demographics:** `Gender`, `SeniorCitizen`, `Partner`, `Dependents`[cite: 18, 19].
* [cite_start]**Account Info:** `Tenure`, `Contract Type`, `Payment Method`, `MonthlyCharges`, `TotalCharges`[cite: 15, 16, 17, 20, 21].
* [cite_start]**Service Usage:** Phone service, Internet service (DSL/Fiber Optic), Tech support, etc[cite: 22].
* [cite_start]**Target Variable:** `Churn` (Yes/No)[cite: 23].

---

## ⚙️ Project Workflow

### 1. Data Preprocessing
* [cite_start]**Missing Values:** Handled blank strings in the `TotalCharges` column by coercing them to numeric and filling with zeros[cite: 26].
* [cite_start]**Feature Encoding:** Applied One-Hot Encoding (`pd.get_dummies`) to convert categorical variables into machine-readable numerical formats[cite: 27].
* [cite_start]**Feature Scaling:** Used `StandardScaler` to normalize continuous variables (`Tenure`, `MonthlyCharges`, `TotalCharges`) to ensure fair weight distribution during modeling[cite: 29].

### 2. Exploratory Data Analysis (EDA)
* [cite_start]**Distribution Analysis:** Visualized the overall churn rate to understand class balance[cite: 31].
* [cite_start]**Risk Segmentation:** Plotted Contract Type vs. Churn Rate to identify vulnerabilities[cite: 32].
* [cite_start]**Correlation:** Generated a feature correlation heatmap to find the strongest mathematical predictors of churn[cite: 34].
* [cite_start]**Business Impact:** Calculated the actual revenue impact, discovering the percentage and dollar amount of monthly revenue lost to churning customers[cite: 35].

### 3. Machine Learning Modeling
[cite_start]Built and evaluated multiple classification models[cite: 38]:
1. **Logistic Regression** (Best Performing Model)
2. **Decision Tree Classifier**
3. **Random Forest Classifier**

[cite_start]**Evaluation Metrics Used:** Accuracy, Precision, Recall, and Confusion Matrix[cite: 40, 41, 42].

---

## 💡 Actionable Business Insights
[cite_start]Based on the data and model predictions, the following recommendations were made to reduce churn[cite: 44, 45, 50]:

1. **Contract Strategy:** Month-to-month contracts are the largest driver of churn. **Recommendation:** Offer incentives (like a 13th month free) for customers to switch to 1-year or 2-year contracts.
2. **Payment Friction:** Electronic Check users churn at a significantly higher rate. **Recommendation:** Incentivize auto-pay via Credit Card with a small monthly discount.
3. **Service Reliability:** Fiber Optic users churn more frequently than DSL users. **Recommendation:** Investigate technical reliability, latency issues, and customer support tickets specifically for the Fiber network.
4. **Onboarding Vulnerability:** New customers (low tenure) are at the highest risk of leaving. **Recommendation:** Implement a specialized 90-day onboarding and engagement program.
5. **Price Sensitivity:** High Monthly Charges heavily correlate with churn. **Recommendation:** Review pricing tiers and offer targeted loyalty discounts to high-value, at-risk customers.

---

## 🚀 How to Run the Project
1. Clone this repository to your local machine.
2. Ensure you have the following Python libraries installed:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
