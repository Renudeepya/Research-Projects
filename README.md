# Credit Card Usage Behavior, Customer Segmentation, and Willingness to Pay: A Comprehensive Analysis

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Pandas](https://img.shields.io/badge/pandas-2.0+-green.svg)](https://pandas.pydata.org/)
[![scikit--learn](https://img.shields.io/badge/scikit--learn-1.3+-orange.svg)](https://scikit-learn.org/stable/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A complete data analytics project that explores credit card customer behavior using descriptive statistics, regression modeling, and unsupervised machine learning (K-Means clustering). The analysis identifies **four distinct customer segments** and provides actionable insights for financial institutions on marketing, product design, and risk management.

## Project Overview

Credit cards are a cornerstone of modern consumer finance, with ~83% of U.S. adults owning at least one. However, customers use them in dramatically different ways — some treat them as convenient payment tools and pay in full monthly, while others revolve large balances or rely on cash advances.

This project applies data science to uncover hidden behavioral patterns, segment customers meaningfully, and estimate willingness to pay. The results help banks move from a one-size-fitsments-all approach to personalized strategies that improve customer satisfaction, increase engagement, and manage credit risk more effectively.

## Objectives

- Characterize major credit card usage tendencies (everyday spending, large purchases, installments, cash advances)
- Analyze balance management and payment behavior
- Model customers’ willingness to pay through spending and utilization patterns
- Segment customers into homogeneous, actionable groups using K-Means clustering
- Provide strategic recommendations for marketing, product design, and risk management per segment

## Dataset Description

The analysis uses the widely-cited **Credit Card Dataset** (8,950 customers) publicly available on Kaggle:

- **Source**: https://www.kaggle.com/datasets/arjunbhasin2013/ccdata  
- **Period**: 6–12 months of transaction and account data  
- **Key features** (17 behavioral variables):

| Variable                | Description                                      |
|-------------------------|--------------------------------------------------|
| `BALANCE`               | Account balance                                  |
| `BALANCE_FREQUENCY`     | How often balance is updated (0–1)               |
| `PURCHASES`             | Total purchase amount                           |
| `ONEOFF_PURCHASES`      | One-time large purchases                         |
| `INSTALLMENTS_PURCHASES`| Installment purchases                            |
| `CASH_ADVANCE`          | Cash withdrawals                                 |
| `PURCHASES_FREQUENCY`   | Frequency of purchases (0–1)                     |
| `CASH_ADVANCE_FREQUENCY`| Frequency of cash advances                       |
| `CASH_ADVANCE_TRX`      | Number of cash advance transactions             |
| `PURCHASES_TRX`         | Number of purchase transactions                  |
| `CREDIT_LIMIT`          | Credit limit                                     |
| `PAYMENTS`              | Total payments made                              |
| `MINIMUM_PAYMENTS`      | Minimum payments made                            |
| `PRC_FULL_PAYMENT`      | Proportion of full payments (0–1)                |
| `TENURE`                | Account tenure in months                         |

No demographic data is included — segmentation is purely behavioral.

## Methodology

1. **Exploratory Data Analysis & Descriptive Statistics**  
2. **Data Preprocessing**  
   - Handling missing values (median/minimum payment imputation)  
   - Log transformation of highly skewed variables  
   - Standardization (StandardScaler)  
3. **Regression Analysis** – Linear model of total purchases vs. credit limit, balance, and tenure  
4. **K-Means Clustering**  
   - Elbow Method, Silhouette Score, and Calinski-Harabasz Index → optimal k = **4**  
   - Final Silhouette Score: **0.408** (moderate-to-good separation)  
5. **Cluster Profiling & Interpretation**

## Results and Insights

### Key Descriptive Findings
- Average balance: ~$1,564 (median $873) → highly right-skewed  
- Only **15%** of customers pay their balance in full regularly  
- Cash advances are rare for most customers (median = $0) but very high for a small group  
- Higher credit limits strongly correlate with higher spending

### Customer Segments (4 clusters)

| Segment                  | Size   | Key Characteristics                              | Business Profile                     |
|--------------------------|--------|--------------------------------------------------|--------------------------------------|
| **High-Engagement Responsible Users** | 37% | High purchases, high balances, pay frequently in full, high credit limits | Most profitable, low risk – ideal for premium cards |
| **Low-Engagement Conservatives**      | 43% | Very low balances & spending, low credit limits, modest full-payment rate | Growth opportunity – activate with rewards & education |
| **High-Spending Revolvers**           | 6%  | Highest balances & purchases, large one-time buys, revolve balances | High revenue + higher risk – monitor closely |
| **Cash Advance Reliant**              | 14% | Moderate purchases, heavy cash advance usage     | Liquidity-constrained, higher risk – offer alternatives |

### Regression Insight (Willingness to Pay)
Higher credit limits are the strongest predictor of total purchases (positive, significant coefficient), confirming that access to credit drives spending behavior.

## Conclusion & Business Implications

This analysis proves that **behavioral segmentation outperforms traditional demographic approaches** for credit card portfolios. Financial institutions can:

- Offer premium rewards cards to Segment 1  
- Run activation campaigns (cashback bonuses) for Segment 2  
- Proactively manage risk and encourage balance pay-down for Segment 3  
- Provide personal loans or lower-fee alternatives to Segment 4 cash-advance users  

Implementing these targeted strategies can increase revenue, improve customer satisfaction, and reduce default risk.

## Technologies Used

- **Python** 3.9+
- **pandas**, **numpy** – data manipulation
- **matplotlib**, **seaborn**, **plotly** – visualization
- **scikit-learn** – preprocessing, regression, K-Means, clustering metrics
- **yellowbrick** – Elbow & Silhouette visualizers
- **Jupyter Notebook** – interactive analysis

