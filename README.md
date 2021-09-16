# Churn-prediction-in-banking
The data is from https://www.kaggle.com/sakshigoyal7/credit-card-customers

This is a customer churn prediction in bank industry, there are 4 models used in this notebook and the best model is XGBoost Classifier with accuracy 0.97 

## Findings:

* There are 3 features with strong correlation :
  * Avg_Open_To_Buy and Credit_Limit (correlation: 1). It can be concluded that the higher the credit limit,  the consumers more open to buy the credit.
   
  ![image](https://user-images.githubusercontent.com/86004756/133546166-a388826b-3b4e-4346-ae10-6869440bbe18.png)
  * Customer_Age and Months_on_book (correlation: 0.79). It can be concluded that older customers have more relationship with bank (the older customer tend to take the loans).
  
  ![image](https://user-images.githubusercontent.com/86004756/133546298-fd02438a-6c28-4c43-8afa-c8b371e1b0cb.png)
  * Avg_Utilization_Ratio and Total_Revolving_Bal (correlation: 0.62). It can be concluded that customers revolving balance will increase along with the high utilization of their card.
  
  ![image](https://user-images.githubusercontent.com/86004756/133546335-1cab8248-6d7b-4366-80af-ad6b3dcef36e.png)

* From the categorical variable 16.07% of the customers leave the bank and majority is female, the pattern of each feature is the same : majority graduate, married, income less than $40K and their card category is blue.

![image](https://user-images.githubusercontent.com/86004756/133546471-e85e2f94-62b6-401e-9760-f63797b8fdc1.png), ![image](https://user-images.githubusercontent.com/86004756/133546506-99d7ed73-0ac8-41f9-9706-c853c34d7b39.png), ![image](https://user-images.githubusercontent.com/86004756/133546577-494ab7f2-a1c3-4810-816c-2d6ac27b2cbd.png), ![image](https://user-images.githubusercontent.com/86004756/133546602-cd917d01-dd77-4ef3-9fc3-0d2b30ceb679.png), ![image](https://user-images.githubusercontent.com/86004756/133546619-f57f24a2-1c8a-4437-a9a2-4999f112b8e2.png)

* From the numerical variable the pattern is slightly different because the attrited customers tend to not use their card anymore.

![image](https://user-images.githubusercontent.com/86004756/133547422-4f49bc98-fad5-468a-8d5d-55303aa91766.png), ![image](https://user-images.githubusercontent.com/86004756/133546849-b4458496-f19f-4430-8505-c089a24aab2a.png), ![image](https://user-images.githubusercontent.com/86004756/133547029-f334ff1b-6107-4072-850c-2bad73ebd890.png)

* There is interesting part where male customer have higher credit limit than the female but their average utilization lower than female customer. Maybe because majority of the customer were female so their utilization is higher.
![image](https://user-images.githubusercontent.com/86004756/133547094-ae1f0c0b-8791-408b-a042-71f50a72846c.png), ![image](https://user-images.githubusercontent.com/86004756/133547056-8bb57b5b-32a1-4a28-a9a7-57e850242410.png)
