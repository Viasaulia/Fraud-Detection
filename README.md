# ***Fraud-Detection***
Looking for best approaches to address imbalance dataset

## About Our Data
Get the data here = https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Except for the time and amount we don't know what the other columns are about (due to privacy reasons). But according to data source, these unknown columns have
been scaled already. Most of the transactions were Non-Fraud 99.8% of the time, while Fraud transactions occurs only almost 0.2%.

## Data Prep
1. Stratified KFold
2. Handling Duplicate
3. Scaling

## Modelling
1. Create baseline using Logistic Regression without oversampling
2. Logistic Regression with wrong way of oversampling
3. Oversampling (SMOTE) being done as part of cross validation, tested on Logistic Regression, Random Forest, Decision Trees and XGBoost
4. Looking on alternative metric such as Precision-Recall Curve (PRC)

## Conclusion
According to AP Score, Logistic Regression with SMOTE provides best performances than other models. Applying SMOTE before cross validation will lead to data leakage. Instead, apply SMOTE during cross validation, we can use Pipeline to make things easier.
