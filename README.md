## Customer-Churn-Prediction-Using-Logistic-Regression
# End-to-end customer churn analysis using Python, EDA, and Logistic Regression to support data-driven retention strategies.

# Project Overview
Customer churn occurs when customers stop using a company’s services.
This project focuses on analyzing customer behavior and predicting churn using historical data and a Logistic Regression model, enabling businesses to take proactive retention actions.

# Objective
Understand customer behavior patterns through data analysis
Identify key factors influencing customer churn
Build a predictive model to classify customers as Churn or Not Churn

# Dataset Description
The dataset contains customer demographic, usage, and interaction details.

# Key features include:
Tenure – Duration of the customer’s relationship with the company
Total Spend – Total amount spent by the customer
Support Calls – Number of times a customer contacted support
Contract Length – Subscription duration
Subscription Type – Type of plan subscribed
Usage Frequency – Service usage intensity
Churn – Target variable (1 = Churn, 0 = Not Churn)

# Exploratory Data Analysis (EDA)
Distribution of Customer Tenure.
Most customers are concentrated in the lower tenure range.
Early-stage customers are more vulnerable to churn.
Highlights the importance of onboarding and early engagement.

# Tenure vs Churn
Non-churned customers generally have higher tenure
Churned customers tend to leave during the early lifecycle
Confirms tenure as a key churn driver

# Distribution of Total Spend
Total spend is right-skewed
Majority of customers have lower spend
A small segment contributes high revenue and should be prioritized for retention

# Total Spend vs Churn
Non-churned customers show higher spending
Churned customers typically have lower spend
Indicates high-value customers are more loyal

# Support Calls vs Churn
Churned customers generally make more support calls
Frequent support interactions indicate dissatisfaction
SupportCalls is a strong churn indicator

# Tenure vs Total Spend by Churn Status
Positive relationship between tenure and spending
Churned customers are concentrated at low tenure and low spend
Churn commonly occurs early in the customer lifecycle

# Churn Rate by Contract Length
Short-term contracts have higher churn rates
Churn decreases as contract length increases
Encouraging long-term contracts can improve retention

# Churn Rate by Subscription Type
Churn rates vary across subscription plans
Some plans show higher churn, indicating potential value or pricing issues
Helps identify plans that need improvement

# Correlation Heatmap
Tenure and Total Spend show a positive correlation
Support Calls show a positive relationship with churn
Helps identify important features and check multicollinearity

# Data Preprocessing & Feature Scaling
Numerical features were standardized using StandardScaler
Scaling ensures all features contribute equally to the model
The scaler was fit on training data only to prevent data leakage

# Model Training
Logistic Regression was used for churn prediction
Chosen for interpretability and suitability for binary classification
Model trained on scaled features with max_iter=1000 for convergence
Outputs probability-based predictions useful for business decisions

# Model Evaluation
Classification Performance
Accuracy: 86%
Recall (Churn): 85%
Precision (Churn): 85%
Balanced performance across both churn and non-churn classes

# Confusion Matrix
[[5891,  885],
 [ 906, 5193]]

# Interpretation:
True Positives (5193): Churn customers correctly identified
False Negatives (906): Churn customers missed
True Negatives (5891): Loyal customers correctly classified
False Positives (885): Loyal customers incorrectly flagged

The model successfully identifies 85% of churn customers, which is critical for effective retention strategies.

# Business Insights
Churn is more likely during the early customer lifecycle
High support call frequency strongly indicates dissatisfaction
Customers on longer contracts churn less
Low-spending customers are at higher risk of churn

# Conclusion
The Logistic Regression model provides strong and interpretable results for churn prediction.
With balanced precision and recall, the model effectively identifies customers at risk of churn and supports data-driven business decisions.

# Tools & Technologies
Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
