# Churn-prediction-on-banking
The data is from https://www.kaggle.com/sakshigoyal7/credit-card-customers

This is a customer churn prediction on bank, there are 4 models used in this notebook and the best model is XGBoost Classifier with accuracy 0.97 

## Findings:

* There are 3 features with strong correlation :
  * Avg_Open_To_Buy and Credit_Limit (correlation: 1). It can be concluded that the higher the credit limit,  the consumers more open to buy the credit.
  * Customer_Age and Months_on_book (correlation: 0.79). It can be concluded that older customers have more relationship with bank (the older customer tend to take the loans).
  * Avg_Utilization_Ratio and Total_Revolving_Bal (correlation: 0.62). It can be concluded that customers revolving balance will increase along with the high utilization of their card.
* From the categorical variable we can see that 16.07% of the customers leave the bank and majority is female, the pattern of each feature is the same : majority graduate, married, income less than $40K and their card category is blue.
* From the numerical variable the pattern is slightly different because the attrited customers tend to not use their card anymore.
