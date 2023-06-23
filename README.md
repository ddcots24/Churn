# Churn Analysis With Predictive Modeling

## Overview
- Created Machine Learning Classification Models using Python to predict customer churn
- Telecommunications company interested in understanding how many and what type of customers likely to leave phone service
  
## Business Understanding
- SyriaTel telecommunications company has data on historical customer usage and churn
- Tasked with building a model to predict future churn of customers
- Insights and recommendations obtained from our predictive model:
  -  Overal expected churn
  - What types of customers are likely to leave
  - Changes to the business model to retain these customers in the future


## Data Understanding and Preperation
- Obtained Data from Kaggle on customer location, phone usage information and historical churn
- Imported into a Pandas dataframe to analyse and clean towards modeling
- Types of inputs are total call minutes, number of calls to customer service, international phone plan etc.
- Took out meaningless and reduntant data from dataframe
- Split into a Training data set and Test data set
  
![Churn Distribution](https://github.com/ddcots24/Churn/assets/131708046/b143fa3e-9c7b-4281-afda-a20b47d3a820)

## Modeling
- Iterated through Logistic Regression, Random Forest and XGBoost classification models to find best results
- Built data pipeline for column transformations, cross validation and hyperparameter tuning
- Mosted interested in "Recall" classification metric to focus on not missing actual churn customers
- Our XGBoost model yielded the best results

## Model Evaluation
![Confusion Matrix](https://github.com/ddcots24/Churn/assets/131708046/6c7519f3-4b3c-4fae-af74-f2a5833c40be)
- Our Final model had a recall score of .86 on the 1 class (churn is true)
- It was important to focus on recall based on our business understanding
    - We want to have a lower false negative rate (predicting that customers arent churning when they actually are) to be able to predict the most amount of true churners
    - Having a higher false positive rate is okay in this case. It means that we are predicting that customers are churning when they actually are staying with the company
    - This might be a slight inconvenience to our staying customers when we reach out to them to see if they are going to churn but it is better to overstimate to keep retention of clients
    - 
***Comparing the fit of our models***
![ROC](https://github.com/ddcots24/Churn/assets/131708046/74d09daf-f1ce-4dc3-82ec-723a0350156d)

## Recommendations
![Feature importance](https://github.com/ddcots24/Churn/assets/131708046/f2eb6876-3f5a-43dd-aad4-ca672fe0ab79)
- With our model predictions we will be able to forecast cutsomer base and be able set expectations on upcoming revenue
- A feature that had great impact on churn rate was the amount of time someone spent on the phone. The amount of time spent on the phone was related to charge
   - Recommend to implement phone plan options to accomodate those with higher usage
- Customer service was another big impact area for churn
    - Recommend to improve customer service experience/ train customer service agents better
- Area Code 510 - east bay San Francisco was another feature that we noticed had a big impact on churn
    - Recommend to offer a specialize service to this region
        - There are potentially a lot of Syrians in this region who have been using Syriatel but have found a better external option











[Presentation](https://github.com/ddcots24/Churn/blob/main/Churn%20Presentation.pdf)
