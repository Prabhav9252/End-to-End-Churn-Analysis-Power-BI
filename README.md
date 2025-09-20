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
Churn Rate: ~17.5% of total customers.
Implication: High churn for a subscription business → urgent need for targeted retention strategies.
2. Demographic Insights
Key Segment at Risk:
Female customers aged 50+ show significantly higher churn.
Primary reasons might include that competitor are offering betters offers as well as better devices.
Recommendation:
Design loyalty campaigns for senior female customers.
Introduce device upgrade programs and exclusive bundled deals.
3. Account Information
Contract Type:
Month-to-month contracts shows the highest churn rate which contributes around 51%.
Annual contracts show much lower churn.
📌 Recommendation: Incentivize customers to migrate to annual/long-term plans (e.g., discounts, free months).
Tenure:
Customers with <6 months tenure churn the most.
After 24 months, churn stabilizes.
📌 Recommendation: Focus on onboarding and engagement in the first 6 months to reduce early exits.
Payment Methods:
Higher churn in electronic check payments.
📌 Recommendation: Encourage auto-pay/credit card adoption with small perks.
4. Geographic Insights
Top 5 states consistently show the highest churn, regardless of demographics.
📌 Recommendation: Launch regional retention campaigns and prioritize service quality improvements in these states.
5. Churn Drivers
Competitor Impact:
180 customers churned due to better devices from competitors.
183 churned due to better offers.
📌 Recommendation: Launch competitive upgrade programs and promotional offers to counter competitor pull.
6. Service Insights
Low Adoption = Higher Churn Risk:
Customers not using device protection, online backup, online security, streaming music churn more often.
These services increase customer stickiness.
📌 Recommendation: Cross-sell these services aggressively.
High Adoption but High Churn = Quality Issues:
Services like Internet, Unlimited Data, Paperless Billing, Phone Services show churn despite high usage.
📌 Recommendation: Conduct service quality audits and improve customer experience in these areas.
7. AI & Predictive Insights
AI narrative visuals confirm trends (e.g., age >50 churn risk).
Planned Random Forest machine learning model will predict future churners at an individual customer level.
📌 Recommendation: Use ML predictions to proactively target at-risk customers before they leave.
### ✅ Strategic Recommendations
1. Focus on early tenure – strong onboarding, engagement in first 6 months.
2. Promote long-term contracts – reduce churn by locking in customers.
3. Target female customers 50+ – personalized offers, device upgrade programs.
4. Compete on devices & bundles – match competitor offers.
5. Improve service quality – especially internet & phone.
6. Leverage cross-sell – push security/backup/entertainment services.
7. Geographic campaigns – focus on top churn states.
8. Adopt predictive churn modeling – use Random Forest ML model for proactive retention.
