Churn Prediction Data Analysis

Overview

This project focuses on analyzing a customer dataset to understand patterns of churn. The analysis involves exploratory data analysis (EDA), data cleaning, feature engineering, and data visualization to gain insights into customer behavior and improve churn prediction.

Dataset

The dataset contains multiple features related to customer demographics, transactions, and account balances. Key columns include:

churn: Target variable indicating whether a customer has churned.

age: Age of the customer.

gender: Gender of the customer.

dependents: Number of dependents.

occupation: Customer's occupation.

city: City of residence.

customer_nw_category: Network category of the customer.

current_balance, previous_month_balance: Financial balance data.

current_month_credit, previous_month_credit: Credit transaction data.

current_month_debit, previous_month_debit: Debit transaction data.

last_transaction: Last transaction date.

Steps Performed

1. Data Loading and Exploration

The dataset is loaded using Pandas.

Initial structure and summary statistics are displayed using .info(), .describe(), and .dtypes.

Missing values are checked using .isnull().sum().

2. Data Visualization

Churn distribution visualization using seaborn.countplot().

Age distribution analysis with sns.histplot().

Gender distribution bar chart with missing value handling.

Dependents outlier detection and imputation using median.

Occupation distribution visualization using a pie chart.

City-wise customer and churn distribution bar plots.

Customer network category distribution and correlation with churn.

3. Data Cleaning and Feature Engineering

Missing values in gender, occupation, and city are replaced with 'Unknown'.

last_transaction is converted to days_since_last_transaction.

Missing values in days_since_last_transaction are imputed with the mean.

New financial metrics are created:

percentage_change_balance: Change in balance compared to the previous month.

total_credit and total_debit: Sum of transactions.

credit_to_debit_ratio: Ratio of credit to debit.

savings_ratio: Current to previous month balance ratio.

credit_to_balance_ratio: Credit transactions relative to balance.

balance_change_Q1_to_Q2 and balance_comparison_Q1_to_current.

4. Encoding Categorical Variables

gender and occupation are one-hot encoded due to low cardinality.

city is frequency encoded due to high cardinality.

Tools & Libraries Used

Python: Core programming language

Pandas: Data manipulation and analysis

Matplotlib & Seaborn: Data visualization

Conclusion

This analysis provides insights into customer churn patterns, feature correlations, and data preprocessing strategies to enhance predictive modeling. Future work includes building a machine learning model to predict churn using the engineered features.

How to Use

Ensure Python and required libraries (pandas, numpy, matplotlib, seaborn) are installed.

Load the dataset and run the provided scripts for EDA and feature engineering.

Modify and extend the analysis based on business requirements.

