# Telecommunication Customer Churn Analysis

## Overview
This work presents a comprehensive analysis of customer churn in the telecommunications sector. Utilizing a dataset of customer attributes and service subscriptions, I apply survival analysis to understand the factors affecting churn risk and identify the most valuable customer segments. The analysis is performed using Python, leveraging libraries such as Pandas, Matplotlib, Seaborn, and Lifelines.

## Jupyter Notebook for Analysis
To view the codes and results of this analysis, please run the Jupyter Notebook named `"MA_HMW3_Survival_Analysis_Hakob_Janesian.ipynb"`. This notebook contains the complete implementation of the survival analysis and further insights derived from the `telco.csv` dataset.

## Data Processing
The dataset, `telco.csv`, includes various customer attributes like region, marital status, education level, and service subscriptions. I preprocess the data by:
- Dropping irrelevant columns (e.g., 'ID').
- Transforming the 'churn' column to a binary format for survival analysis.
- Encoding categorical variables into dummy variables, avoiding multicollinearity.
- Replacing zero values in 'tenure' with a small number (epsilon) to facilitate model fitting.

## Survival Analysis
I employ both traditional and Accelerated Failure Time (AFT) survival models, including Weibull, Exponential, LogNormal, and LogLogistic, to analyze customer churn. The models' performance is evaluated using the Akaike Information Criterion (AIC) and Bayesian Information Criterion (BIC), with the LogNormalFitter emerging as the best fit.

## Significant Findings
My analysis reveals several significant factors influencing churn:
- Longer tenure at the same address and older age are associated with decreased churn risk.
- Customers in E-service, Plus service, and Total service categories exhibit delayed churn.
- Internet and voice service subscribers are at a higher churn risk.

## Customer Lifetime Value (CLV) Analysis
I calculate CLV and analyze its distribution across different demographics and service types, revealing:
- Gender does not significantly impact CLV.
- Educational level variations do not significantly affect CLV, but younger or less educated groups show higher engagement.
- Married customers tend to have higher and more consistent CLVs.

## Valuable Customer Segments
Based on CLV and churn risk, the most valuable segments are identified as:
- Customers subscribed to Plus Service and E-Service.
- Married customers, particularly in Zone 2.

## Retention Budget Calculation
With a survival probability threshold of 0.75, I identified 135 customers at risk of churning within a year. Assuming a retention cost of $150 per customer, the annual retention budget is calculated to be $20250.

## Retention Strategy Recommendations
To enhance customer retention, I suggest:
- Personalized communication and offers based on individual customer profiles.
- Implementing loyalty programs and incentives for long-term contracts.
- Proactive customer service and feedback mechanisms, especially for high-risk segments.

## Conclusion
This analysis provides valuable insights into customer churn in the telecommunications sector, highlighting key factors and customer segments for targeted retention strategies. The approach combines theoretical knowledge with practical experience, offering a robust framework for reducing churn and enhancing customer loyalty.
