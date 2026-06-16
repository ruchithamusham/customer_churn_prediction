# Customer Churn Prediction

## Internship Context
This project was completed as part of my Data Analytics Online Internship 
at Codec Technologies. The goal was to apply end-to-end machine learning 
on a real business problem — predicting which customers are likely to leave 
a telecom company.

## What is this project about?
I used Telco customer data to figure out why customers are churning and 
built a model to predict who is at risk of leaving next. The final output 
includes a risk segmentation — High, Medium, Low — so the business team 
can prioritize which customers to target with retention offers.

## Dataset
- Telco Customer Churn dataset (Kaggle)
- 7043 customer records, 21 columns
- Covers contract type, tenure, monthly charges, services subscribed

## Tools I used
- Python, Jupyter Notebook
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn, XGBoost

## What I did
1. Explored the data to understand churn patterns
2. Fixed TotalCharges column which was stored as object type
3. Encoded categorical columns using get_dummies
4. Trained 3 models — Logistic Regression, Random Forest, XGBoost
5. Compared models using ROC AUC and plotted ROC curves
6. Built feature importance chart to find top churn drivers
7. Assigned each customer a churn risk score and categorized them

## What I found
- Month-to-month contract customers churn the most
- New customers with low tenure are high risk
- Higher monthly charges increase churn probability
- Top churn drivers: Contract type, Tenure, MonthlyCharges

## Model Results
| Model | ROC AUC |
|-------|---------|
| Logistic Regression | 0.83 |
| Random Forest | — |
| XGBoost | — |

Logistic Regression gave the best interpretable results and was used 
for final risk scoring.

## Risk Segmentation Output
Customers were split into 3 categories based on churn probability:
- High Risk — churn probability ≥ 50%
- Medium Risk — churn probability between 30-50%
- Low Risk — churn probability < 30%

## Files in this repo
- `customer_churn_prediction.ipynb` — full notebook
- `WA_Fn-UseC_-Telco-Customer-Churn.csv` — dataset used

## Business Recommendation
Target High Risk customers immediately with retention offers like 
discounts or contract upgrades. Focus especially on month-to-month 
customers with high monthly charges and low tenure.
