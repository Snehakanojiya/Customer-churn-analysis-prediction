# Customer-churn-analysis-prediction
# 📊 Customer Churn Analysis & Prediction

An end-to-end **Customer Churn Analysis and Prediction** project using **SQL, Python, Machine Learning, and Power BI** to identify churn patterns, predict customers at risk, and generate actionable business insights.

---

## 🎯 Project Objective

Customer churn can significantly impact recurring revenue and customer lifetime value.

The objective of this project is to:

- Analyze customer churn patterns
- Identify customer segments with higher churn rates
- Understand the relationship between churn and customer demographics, tenure, contracts, payments, and services
- Build a machine learning model to predict customers likely to churn
- Identify customers at risk of churn
- Create an interactive Power BI dashboard for business decision-making

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **SQL** | Data cleaning, transformation and analysis |
| **Python** | Data preprocessing and machine learning |
| **Pandas** | Data manipulation |
| **NumPy** | Numerical analysis |
| **Scikit-learn** | Machine learning |
| **Random Forest** | Churn prediction |
| **Matplotlib & Seaborn** | Data/model visualization |
| **Power BI** | Interactive dashboards |
| **Jupyter Notebook** | Machine learning development |

---

## 🔄 Project Workflow

```text
Customer Data
     ↓
SQL Data Cleaning & Transformation
     ↓
Exploratory Data Analysis
     ↓
Feature Preparation & Encoding
     ↓
Random Forest Classification
     ↓
Model Evaluation
     ↓
Predict At-Risk Customers
     ↓
Power BI Dashboard
     ↓
Business Insights & Recommendations
🗄️ SQL Analysis

SQL was used to prepare, transform, validate, and analyze the customer data.

Key SQL Activities
Customer analysis by gender
Customer analysis by contract type
Customer revenue analysis by customer status
State-level customer analysis
Missing/null value analysis
Handling missing values using ISNULL
Creation of production customer data
Creation of churn/stayed customer view
Creation of joined customer view

The SQL workflow creates a production-level churn table and separates customers who have Stayed/Churned from newly Joined customers for prediction.
🤖 Machine Learning – Churn Prediction

A Random Forest Classifier was developed to predict whether a customer is likely to churn.

Data Preparation

Categorical variables were encoded using LabelEncoder.

The target variable was converted into:
Stayed  → 0
Churned → 1
The dataset was divided into:

80% Training Data
20% Testing Data
random_state = 42

Model Used
Random Forest Classifier

n_estimators = 100
random_state = 42
The Random Forest model was trained on the customer data and used to predict customer churn.

Model Evaluation

The model was evaluated using:

Accuracy
Precision
Recall
F1-Score
Confusion Matrix
Feature Importance

Model Performance
| Metric          |   Score |
| --------------- | ------: |
| Accuracy        | **84%** |
| Churn Precision | **78%** |
| Churn Recall    | **65%** |
| Churn F1-Score  | **71%** |

The model provides a useful approach for identifying customers who may be at higher risk of churn and can support targeted customer-retention strategies.

Confusion Matrix
                 Predicted
              Stayed  Churned
Actual Stayed    783      64
Actual Churned   126     229

Prediction of At-Risk Customers

After training and evaluating the model, the model was applied to newly joined customers.

The prediction workflow:
Joined Customers
       ↓
Remove Non-Predictive Columns
       ↓
Encode Categorical Variables
       ↓
Random Forest Model
       ↓
Churn Prediction
       ↓
Filter Predicted Churners
       ↓
Customer-Level At-Risk List

💡 Key Business Insights

The analysis can help businesses understand:

Which customer segments are more likely to churn
How contract types relate to customer churn
Which customer characteristics are associated with churn
Geographic differences in customer behavior
Revenue associated with different customer statuses
Which newly joined customers may require additional attention
🎯 Business Recommendations

Based on the analysis and prediction workflow, businesses can:

Identify high-risk customers earlier
Develop targeted retention campaigns
Focus retention efforts on high-risk customer segments
Monitor customers with characteristics associated with churn
Use predictive insights to prioritize customer outreach
Combine churn predictions with customer value to improve retention strategies
