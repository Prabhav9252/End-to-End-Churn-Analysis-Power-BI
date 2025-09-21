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

<img width="1149" height="644" alt="image" src="https://github.com/user-attachments/assets/31654eda-efa5-4a4c-8a9b-7d1843a9d697" />


## Predicting Customer Churn
To add a predictive layer to the churn analysis, this project includes a machine learning model to identify customers who are likely to churn in the future. This allows for proactive measures to improve customer retention.
### 1. Machine Learning Algorithm: Random Forest
The prediction model was built using the Random Forest algorithm. Random Forest is a popular machine learning technique that operates by constructing multiple decision trees during training. Each tree is trained on a random subset of the data and features. The final prediction is determined by a majority vote from all the individual trees, which enhances the model's accuracy and reduces the risk of overfitting. This algorithm was chosen for its simplicity and widespread use in churn analysis.
### 2. Data Preparation for the Model
Before building the model, the data was prepared and exported from the SQL Server database.
• Two specific views, vw_ChurnData (for training and testing) and vw_JoinData (for new predictions), were created in SQL Server.
• These views were imported into an Excel file named Prediction_Data.xlsx. This file served as the data source for the Python-based machine learning model.
### 3. Building the Prediction Model in Python
The machine learning model was developed using Python in a Jupyter Notebook environment. Key libraries such as pandas, NumPy, scikit-learn, and joblib were used for data manipulation, model creation, and evaluation.
The process involved several key steps:
• Data Loading: The vw_ChurnData sheet was loaded into a pandas DataFrame.
• Data Preprocessing:
    ◦ Irrelevant columns like Customer_ID, Churn_Category, and Churn_Reason were dropped to avoid bias and data leakage.
    ◦ Categorical features were converted into numerical values using LabelEncoder from scikit-learn, as machine learning models work with numerical data.
    ◦ The target variable, Customer_Status, was manually encoded, with 'Churned' mapped to 1 and 'Stayed' mapped to 0.
• Train-Test Split: The dataset was split into training (80%) and testing (20%) sets to train the model and then evaluate its performance on unseen data.
• Model Training: A RandomForestClassifier was initialized (with n_estimators=100) and trained on the training data (X_train, y_train).
### 4. Model Evaluation
After training, the model's performance was evaluated on the test dataset.
• Confusion Matrix: The model's predictions were compared against the actual outcomes.
    ◦ True Negatives (Correctly predicted 'Stayed'): 783
    ◦ False Positives (Incorrectly predicted 'Churned'): 64
    ◦ False Negatives (Incorrectly predicted 'Stayed'): 126
    ◦ True Positives (Correctly predicted 'Churned'): 229
• Classification Report: This provided detailed metrics.
    ◦ The model achieved an overall accuracy of 84%.
    ◦ Precision for predicting churn was 78%, while recall was 65%.
    ◦ The model performed better at predicting customers who would stay, which might be due to the imbalanced nature of the dataset (more 'Stayed' instances than 'Churned').
• Feature Importance: An analysis was conducted to determine which features had the most impact on predicting churn. This can be used to fine-tune the model by removing less important features.
### 5. Predicting Churn on New Data
Once trained and evaluated, the model was used to predict churn on a new dataset (vw_JoinData), which contained newly joined customers.
1. The new data was loaded and preprocessed using the same label encoders saved from the training phase.
2. The trained Random Forest model (rf_model) made predictions on this new data.
3. The final output, containing only the customers predicted to churn (predicted value of 1), was saved to a new CSV file named Predictions.csv.
This final CSV file was then imported into Power BI to create a dedicated "Churn Prediction" dashboard page, visualizing the profile of customers at high risk of churning

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
