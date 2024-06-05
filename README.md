# machine_learning_ArabianUsedCarsSales
## Context
Syarah is a cars sales company based in Riyadh, Saudi Arabia. The company specializes in promoting the sale of new and used cars, assisting companies and people in purchasing or selling their vehicles as easily and quickly as possible. Syarah provides an online car marketplace through their mobile application and website, syarah.com, there users could look through their catalogue of cars that are on sale. Alternatively, users who want to sell their cars through Syarah can submit a form, filled with details of their car. Then users will bring their car to Syarah to have it inspected and then put it up in Syarah's catalogue of used cars for sale.

## Problem Statement
In order for a car to be put in Syarah's catalogue, Syarah needs to first inspect the car then evaluate its price. Syarah will bear the cost of the inspection and not charge it on the user. The inspection cost of around [200](https://syarah.com/en/about-us/services) SAR. Thus if a user has their car inspected and receive a price they do not find satisfying and reject having their car enter Syarah's catalogue, then Syarah has lost 200 SAR. This analysis proposes a machine learning model that could predict the potential price of a car based on car features users provided through the form they submitted with cars already on Syarah's catalogue as training data. This way, Users can get an idea of what price they could sell their car and make a decision whether to go through with Syarah or look somewhere else and save Syarah time and money by reducing the amount of customers that would cancel after inspection.

## Stakeholders 
- Syarah

## Goals:
- Create a machine learning model that could predict a car's price as accurately as possible based on car features taken from Syarah's used car catalogue
- Identify which factors that would affect the predicted price of a car
  
## Analytic Approach:
- Analyze the data to better understand the data and the value ranges of each feature/column

- Prepare the data by cleaning the data from missing and duplicate values a

- Determine which preprocessing methods to use for each feature and create a column transformer and pipeline

- Determine which estimator has the best performance based on evaluation metric, specifically Mean Absolute Error

- Perform hyperparameter tuning to the best estimator to improve model performance

- Evaluate model using evaluation metrics, namely Mean Absolute Error, Root Mean Squared Error, Mean Squared Error, and Mean Absolute Percentage Error

- Conduct residual analysis to better understand model performance and limitation.

- Perform model summary using SHAP to determine which features significantly impact car price prediction.

## Tabel Description
Attribute Information
|Attribute|Description|
| --- |  --- |
|Type|Type of used car|
|Region|The region in which the used car was offered for sale.|
|Make|The company name.|
|Gear_Type|Gear type size of the used car.|
|Origin|Origin of the used car.|
|Options|Options of the used car.|
|Year|Manufacturing year.|
|Engine_Size|The engine size of the used car.|
|Mileage|Mileage of the used car|
|Negotiable|True if the price is 0, that means it is negotiable.|
|Price|Used car price.|

## Conclusion
According to the model, `Year`, `Engine_Size`, dan `Mileage` are the features that affect used car price prediction the most,

Light Gradient Boosting Machine is the best among several base machine learning models, and its performance improved after conducting hyperparameter tuning.

The evaluation metric used on the model are R2, RMSE, MAE, and MAPE. Based on the MAPE score the model produced, which is 20.91%, we can conclude that when implemented and imputed with data within the set limitations (Mileage: 100 - 487,100,Engine_Size: 1.0 - 9.0,Year: 2004 - 2021) it can predict the price of a car with an error around 20.91%.

However, it is not improbable that the error of the prediction increase because of the bias produced by the model as seen by the visualization between the actual price and the predicted price. The bias is caused by the lack of data with car prices between 180,000 to 850,000 as well as several features with sparse categorical values like `type`,`make`, and `region`. 

## Video Presentation
https://drive.google.com/drive/u/0/folders/1BslhZreXivJ_BltQtxWvPzzSqGazzWrn
