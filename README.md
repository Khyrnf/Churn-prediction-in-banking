# Churn-prediction-in-banking
The data is from https://www.kaggle.com/sakshigoyal7/credit-card-customers

This is a customer churn prediction in bank industry, there are 4 models used in this notebook and the best model is XGBoost Classifier with accuracy 0.97 

## Findings:

* There are 3 features with strong correlation :
  * Avg_Open_To_Buy and Credit_Limit (correlation: 1). It can be concluded that the higher the credit limit,  the consumers more open to buy the credit.
   
  <img src= "https://user-images.githubusercontent.com/86004756/133546166-a388826b-3b4e-4346-ae10-6869440bbe18.png" width="250" height="250">
  
  * Customer_Age and Months_on_book (correlation: 0.79). It can be concluded that older customers have more relationship with bank (the older customer tend to take the loans).
  
  <img src= "https://user-images.githubusercontent.com/86004756/133546298-fd02438a-6c28-4c43-8afa-c8b371e1b0cb.png" width="250" height="250">
  
  * Avg_Utilization_Ratio and Total_Revolving_Bal (correlation: 0.62). It can be concluded that customers revolving balance will increase along with the high utilization of their card.
  
  <img src= "https://user-images.githubusercontent.com/86004756/133546335-1cab8248-6d7b-4366-80af-ad6b3dcef36e.png" width="250" height="250">

* From the categorical variable 16.07% of the customers leave the bank and majority is female, the pattern of each feature is the same : majority graduate, married, income less than $40K and their card category is blue.

<img src= "https://user-images.githubusercontent.com/86004756/133546471-e85e2f94-62b6-401e-9760-f63797b8fdc1.png" width="250" height="200">, <img src= "https://user-images.githubusercontent.com/86004756/133546506-99d7ed73-0ac8-41f9-9706-c853c34d7b39.png" width="250" height="200">, <img src= "https://user-images.githubusercontent.com/86004756/133546577-494ab7f2-a1c3-4810-816c-2d6ac27b2cbd.png" width="250" height="200">, <img src= "https://user-images.githubusercontent.com/86004756/133560495-ef3a51a1-6635-4d1f-bc5b-4b905d18c2ff.png" width="250" height="200">, <img src= "https://user-images.githubusercontent.com/86004756/133546619-f57f24a2-1c8a-4437-a9a2-4999f112b8e2.png" width="250" height="200"> 

* From the numerical variable the pattern is slightly different because the attrited customers tend to not use their card anymore.

<img src= "https://user-images.githubusercontent.com/86004756/133547422-4f49bc98-fad5-468a-8d5d-55303aa91766.png" width="250" height="200">, <img src= "https://user-images.githubusercontent.com/86004756/133546849-b4458496-f19f-4430-8505-c089a24aab2a.png" width="250" height="200">, <img src= "https://user-images.githubusercontent.com/86004756/133547029-f334ff1b-6107-4072-850c-2bad73ebd890.png" width="250" height="200">

* There is interesting part where male customer have higher credit limit than the female but their average utilization lower than female customer. Maybe because majority of the customer were female so their utilization is higher.

<img src= "https://user-images.githubusercontent.com/86004756/133547094-ae1f0c0b-8791-408b-a042-71f50a72846c.png" width="250" height="200">, <img src= "https://user-images.githubusercontent.com/86004756/133547056-8bb57b5b-32a1-4a28-a9a7-57e850242410.png" width="250" height="200">

## Model Building :
First, I do some encode for the categorical variables ordinal with replace (based on the level) and nominal with dummy. I also split the data into train and tests sets with a test size of 30%.

I tried four different models and evaluated them using accuracy, recall and precision. then i use gridsearchCV to select the best parameter and use recall for the scoring  because it gives a measure of how accurately our model is able to identify the relevant data.

## Model Performance:
The XGBoost Classifier model perform the highest recall.

![image](https://user-images.githubusercontent.com/86004756/133558811-955b9193-907b-4cd1-935f-ed3e8115498e.png)
