# Insurance-Cross-Sell-Prediction
This project aims to provide the best model for predicting the likelihood of a customer opting for the Vehicle policy
## Problem Statement
When a Health Insurance company wants to add a Vehicle policy business to its portfolio, an analysis should be made to understand how well the business would perform in real time. This can be done by collecting some data from existing customers and understanding if they would show interest in buying their new product. Our project aims to provide the best model for predicting the likelihood of a customer opting for the Vehicle policy.

## Data sources:
Fetched data from Kaggle. The dataset consists of approximately 380,000 rows and 12 columns of data related to existing customers and their vehicles.
The data has 11 input columns and 1 output column as specified below.

Inputs:

<br />•	Gender – If Male it’s stored as 1 and for Females, it is 0
<br />•	Previously insured – If the customer is already insured, Previously insured is stored as 1. Otherwise, it’s 0
<br />•	Vehicle Age – Age of the Vehicle 
<br />•	Vehicle Damage – If the vehicle is damaged previously, it’s stored as 1. If the vehicle is never damaged, it’s stored as a 0
<br />•	Driving License – If the customer has a driving license, it’s stored as 1. Otherwise, it’s stored as a 0
<br />•	Annual Premium – Premium that customer has to pay for the new policy
<br />•	Vintage – Number of days the customer has been associated with the company
<br />•	Region code – Code of the region that customer lives in
<br />•	Age – The age of the customer
<br />•	Policy Sales Channel – Channel the customer was approached. Examples – email, telephone
<br />•	ID – unique ID of the customer

Outputs:

<br />•	Response – If the customer is interested in taking a new vehicle Policy, the response is stored as 1. Zero otherwise
The dataset has categorical columns such as Gender, Previously Insured, Vehicle Age, Region Code, Policy Channels, and Vehicle Damage. The rest are numerical columns.
Dataset link: https://www.kaggle.com/datasets/anmolkumar/health-insurance-cross-sell-prediction

## Data Preparation:
<br />• Ordinal encoding and One hot encoding 
<br />• Scaling techniques such as Minmax scaling and Standard scaling 
<br />• Sampling methods such as Random Oversampled, Random Undersampled, and SMOTE 

## Data Visualization:
The Correlation heatmap has been plotted for different variables 
<br />•Age vs Response
<br />• Previously Insured vs Response
<br />• Region code vs Response
<br />• Policy Sales Channel vs Response
<br />• Driving license vs response
<br />• Vehicle damage vs response
<br />• Gender vs response
<br />• Vintage vs response
<br />• Vehicle age vs response

## Data Modeling
Have used three Machine Learning models in this project. They are as below
<br />1.	Logistic Regression
<br />2.	KNN Classifier
<br />3.	Random Forest Classification

## Best Performing model
From the derived results, observed a high F1 score and Recall score for Logistic Regression with Minmax scaled and Random Oversampled data. 


## Key observation:

The model should be having the False Negative count as low as possible. The intuition behind this is, if the model predicts a customer who is actually interested in taking the policy as “not interested”, the company is losing a customer. Whereas, if the model predicts a customer who is not interested in the company as “interested”, it’s not an issue for the company. We observe TN count is very low for Logistic Regression with scaled and sampled data. 

## Recommendations to Decision-makers:
<br />1.	As data contains more observations with negative responses, though the annual premium the company is offering is not impacting response, customers are not showing interest due to other reasons which cannot be controlled by the company. Due to a lack of demand, the company should reconsider the decision in introducing a new product.
<br />2.	Company should come up with better incentives in order to lure customers in opting for their product.
<br />3.	From the graph Visualization graphs, it can be observed that customers living in Region-28 and Region-8 show interest in buying their policy when compared with other regions. It would be ideal to start issuing Vehicle Policies in the mentioned regions and then expand toward other regions.
<br />4.	It can also be observed from the graphs that when the company approached customers through Channel-26 and 124, they received better responses compared to other Channels. We would recommend the company focus on reaching out to customers via these Channels.
<br />5.	From the correlation heatmap, it can be observed that if the customer already has vehicle policy, he is not likely to consider a new policy offered by the company. Hence they can exclude such customers and reach out more to customers who are older in age and customers whose vehicles is damaged in the past. 
<br />6.	Another observation from heatmap is that the Annual premium offered by the company is not a key factor that’s impacting responses. Hence rates need not be lowered.






