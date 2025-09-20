# End-to-End-Churn-Analysis-Power-BI

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/84fae83e-b1ef-48e7-afe7-38a762ba8b32" />

### 🔎 Project Overview

This project demonstrates an end-to-end churn analysis pipeline using SQL Server, Power BI, and Machine Learning (Python). It covers the full lifecycle from ETL and data cleaning → dashboard creation → insights → predictive modeling.

### 🛠 Tech Stack
1. SQL Server – ETL, data storage, cleaning, creating views
2. Power BI – Data modeling, dashboard visualization, AI insights
3. Python (Jupyter Notebook) – Machine learning with Random Forest

### 📂 Project Workflow
1. Data Preparation (SQL Server)
2. Created database & staging tables.
3. Cleaned null values, standardized data types.
4. Built production tables & SQL views for churned/joined customers.
5. Data Exploration (SQL Queries)
6. Distribution checks: gender, contracts, tenure, states.
7. Null analysis & replacements.
8. Created age/tenure group buckets.

Power BI Dashboard

KPIs: total customers, churn count, churn rate, new joiners.

Demographics: gender, age groups.

Account info: payment methods, contract type, tenure.

Geography: top churn states.

Churn drivers: churn category, churn reasons.

Services: adoption vs churn (matrix view).

Interactivity: slicers, tooltips, AI insights.

# 📊 Customer Churn Analysis – Insights & Recommendations
## 🔎 Executive Summary

Our churn analysis identified key customer groups, behaviors, and service factors contributing to a 17.5% churn rate. Insights suggest churn is driven by contract type, competitor offers, early tenure disengagement, and service quality gaps.

1. Overall Churn

The churn rate is around 17.5% of total customers, which is quite high for a subscription-based business. This indicates a serious customer retention issue and urgent corrective actions. Targeted retention strategies and proactive interventions are critical to reducing this churn.

2. Demographic Insights

Female customers aged 50+ have the highest churn rate compared to other groups. The main reasons include competitors offering better devices and more attractive offers. Businesses should focus on designing loyalty campaigns for this segment. Additionally, offering device upgrade programs and exclusive bundles can help retain them.

3. Account Information

Contract Type:
Customers on month-to-month contracts (≈51%) are most likely to churn, while annual contract holders show lower churn. Businesses should incentivize long-term contracts with discounts or free months.

Tenure:
Customers with less than 6 months of tenure churn the most, while churn stabilizes after 24 months. Early engagement and onboarding programs in the first 6 months are crucial.

Payment Methods:
Customers using electronic checks have higher churn rates. Encouraging auto-pay or credit card payments with small rewards can improve retention.

4. Geographic Insights

The top 5 states consistently show the highest churn rates, regardless of customer demographics. This suggests churn is influenced by regional factors, such as service coverage or competitor presence. Organizations should consider regional campaigns tailored to these states. Improving service quality in high-churn areas will have the most impact.

5. Churn Drivers

The biggest driver of churn is competition, with 180 customers leaving for better devices and 183 for better offers. This emphasizes that customers are highly price- and feature-sensitive. Launching competitive upgrade programs can help retain device-driven churners. Similarly, promotional offers can counteract competitors’ deals.

6. Service Insights:-

Low Adoption → High Churn Risk:
Customers who don’t use services like device protection, online backup, online security, or streaming music churn more often. These services create stickiness, so businesses should cross-sell them aggressively.

High Adoption but High Churn → Quality Issues:
Services such as Internet, Unlimited Data, Paperless Billing, and Phone Services show churn despite wide adoption. This suggests dissatisfaction with service quality, requiring audits and improvements.

7. AI & Predictive Insights

AI-driven narrative visuals confirm key risk factors like higher churn in the 50+ age group. The next step is to use a random forest machine learning model to predict churn at the individual level. This predictive approach will help identify at-risk customers proactively. Retention teams can then target these customers with personalized campaigns before they leave.

### ✅ Strategic Recommendations
1. Focus on early tenure – strong onboarding, engagement in first 6 months.
2. Promote long-term contracts – reduce churn by locking in customers.
3. Target female customers 50+ – personalized offers, device upgrade programs.
4. Compete on devices & bundles – match competitor offers.
5. Improve service quality – especially internet & phone.
6. Leverage cross-sell – push security/backup/entertainment services.
7. Geographic campaigns – focus on top churn states.
8. Adopt predictive churn modeling – use Random Forest ML model for proactive retention.
