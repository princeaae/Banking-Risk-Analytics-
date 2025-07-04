# 💼 Risk Analytics in Banking

## Tools Used - MySQL, Python, Power BI

---

## 📌 Table of Contents
1. [🎯 Project Objective](#project-objective)
2. [💡 Business Problem](#business-problem)
3. [📊 Dataset Description](#dataset-description)
4. [🔄 ETL & Data Cleaning (Python)](#etl--data-cleaning-python)
5. [📈 Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
6. [📊 Power BI Dashboard](#power-bi-dashboard)
7. [📌 Business Insights & Results](#business-insights--results)
8. [✅ Conclusion](#conclusion)

---

## 🎯 Project Objective

To build an end-to-end banking analytics system that helps financial institutions:
- Analyze customer deposit and loan behavior
- Identify high-risk clients
- Detect patterns in customer loyalty and engagement
- Enable strategic decision-making through data visualization

---

## 💡 Business Problem

Banks are constantly faced with risk:  
> _"How do we decide which customers are safe to give a loan to?"_

Traditional metrics (income, credit card usage) don’t always give the full picture.  
This project helps banks:
- Profile customers based on income, occupation, nationality, etc.
- Visualize deposit vs loan behavior
- Identify profitable yet risky segments
- Track customer engagement over time

---

## 📊 Dataset Description

The dataset was uploaded to MySQL and contains:
- Customer Demographics (Gender, Nationality, Occupation)
- Financial Metrics (Estimated Income, Savings, Loans, Business Lending, Credit Card Balances)
- Account Types (Checking, Savings, Foreign Currency)
- Fee Structure, Loyalty Classification, and Date Joined

✅ **Rows**: ~3000+  
✅ **Columns**: ~18+  
✅ **Source**: Provided CSV → MySQL → Power BI

---

## 🔄 ETL & Data Cleaning (Python)

### 🔗 Connected Python to MySQL using `mysql.connector`  
Imported data into a Pandas DataFrame for preprocessing.

### 🧹 Data Cleaning Steps:
- Handled missing values (e.g. median imputation for `Credit Card Balance`)
- Converted `GenderId` from (1/2) to ("Male"/"Female")
- Removed duplicates
- Standardized date columns
- Converted income and fee values to numeric

### 🛠 Feature Engineering:
- **Income Banding** (`Low`, `Medium`, `High`) using `pd.cut()`
- **Engagement Days** = Date difference between Join Date and Today
- **Processing Fee Logic** based on Fee Structure

---

## 📈 Exploratory Data Analysis (EDA)

Used `seaborn` and `matplotlib` to explore relationships between:
- Occupation vs Loan
- Nationality vs Deposit Behavior
- Engagement vs Account Type
- Income vs Savings

### 🔍 Correlation Heatmap
Analyzed relationships between numerical fields like:
- Estimated Income
- Bank Loans
- Credit Card Balances
- Superannuation Savings

---

## 📊 Power BI Dashboard

After analysis, data was visualized using Power BI.

### ✅ Pages Created:
1. **Home Dashboard**  
   - Total Clients, Total Loans, Total Deposits  
   - Gender & Income Band Filters  
   ![Home Dashboard](https://raw.githubusercontent.com/princeaae/Banking-Risk-Analytics-/main/home.png)

2. **Loan Analysis**  
   - Loan metrics by Occupation, Income Band, Nationality  
   - Credit & Business Lending Risks  
   ![Loan Analysis](https://raw.githubusercontent.com/princeaae/Banking-Risk-Analytics-/main/loan_data_analysis.png)

3. **Deposit Analysis**  
   - Breakdown of checking, savings, and foreign currency deposits  
   - Insights by Gender and Income  
   ![Deposit Analysis](https://raw.githubusercontent.com/princeaae/Banking-Risk-Analytics-/main/deposit_analysis.png)

4. **Summary Page**  
   - Aggregated KPIs across all areas  
   ![Summary](https://raw.githubusercontent.com/princeaae/Banking-Risk-Analytics-/main/summary.png)

---

## 📌 Business Insights & Results

- **Medium Income Customers** hold the most deposits — lower risk, higher trust.
- **Accountants and Admins** had higher loan amounts and lower deposits → possible red flags.
- **Foreign nationals** borrowed more but had shorter engagement → monitor risk.
- **High Processing Fee** clients contributed significantly to total fee income.
- **Men spent more on credit**, but women saved more on average.

---

## ✅ Conclusion

This project simulates how real banks could use data to reduce credit risk and increase customer value. By using:
- **MySQL** for data structuring
- **Python** for EDA & cleaning
- **Power BI** for storytelling

…we built a system that could help any financial institution make smarter, risk-aware decisions.

---

> ⚙️ **Future Add-on**: Incorporate a machine learning model to predict potential defaulters or churners using historical behavior.

---

👤 **Made by:** Prince Bhatt  
📫 **LinkedIn**: [Prince Bhatt](https://www.linkedin.com/in/prince-bhatt/)  
📂 **GitHub**: [princeaae](https://github.com/princeaae)
