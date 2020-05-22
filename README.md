## Ames Housing Data and Kaggle Challenge
---

### Problem Statement:

Zillow will often indicate "Estimated home price" to inform users about the market rates of homes, even when they are not
yet explicitly for sale. More accurate depictions of home values translates to more confidence in Zillow's product.
Moreover, with better prediction, more reliability on the tool and consequently better user engagement what leads to
greater possibility for advertising revenues.

Using data given on properties sold in Ames, Iowa, my task is to create the best linear regression model to predict the sale
price of properties based on an extensive list of properties features.

After creating models with the given dataset, the model was tested on a new dataset without sale prices. Using the same
techniques to clean the dataset the models were used to predict those prices based on the features selected to run the
regression model on.

The main performance indicator used to evaluate and tune models was the RMSLE (Root Mean Squared Log Error).

### Steps Taken:


### Conclusion:
- Final Model's Performance
  - RMSLE Test= 0.0085
  - R2 Train: 0.9627
  - R2 Test: 0.9275
  - Kaggle Score: 0.11704 RMSLE (Top 11%)

A few different models were trained and final predictions were submitted to Kaggle by using a Voting Regressor as an Ensembling Technique.

### Next Steps and Model Improvement:
- External Input to the Model
- New Imputation Techniques for Null Values
