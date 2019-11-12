## General Assembly DSI 9 - Gabriel Perez Prieto
## Project 2 - Ames Housing Data and Kaggle Challenge

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

The main performance indicator used to evaluate and tune models was the RMSE (Root Mean Squared Error).

### Executive Summary:
- Libraries Import
- Load Dataset
- Data Cleaning
  - Renaming Columns
  - Handling Null Values
  - Transforming Nominal Data to Numerical
  - Null Values Inputting
- EDA (Exploratory Data Analysis)
  - Correlations of Features with Target Variable
  - Visual Representation of Features and Target (Numerical)
  - Checking for Outliers (Numerical Features)
  - Checking Distributions for all Numerical Features
  - Feature Engineering
  - Visual Representation of Features and Target (Nominal)
  - Creating Dummy Variables for Nominal Features
  - Saving Clean Dataset to .csv
- Feature Selection and Model Tuning
  - Checking Model's Performance
- Creating Model
  - Scale Data
  - Instantiate a Linear Regression Model
  - Evaluate Model
- Regularization
  - Ridge
  - Lasso
- Kaggle Submission

### Conclusion:
Two final models were created
- Model_1
  - 49 Features
  - RMSE = 0.145
  - R2 Train: 0.876
  - R2 Test: 0.894
  - Ridge Regularization
  - Kaggle Score: 24,001

- Model_2
  - 1850 Features
  - RMSE = 0.094
  - R2 Train: 0.923
  - R2 Test: 0.963
  - Lasso Regularization
  - Kaggle Score: 19,200

Model_1 is a Multiple Linear Regression Model with 49 Features that were the most correlated features with the
target variable (Sale Price), by interaction terms between existing variables and one hot encoding for the
Neighborhoods feature. The model responded better to the Ridge Regularization on Kaggle despite showing no signals
of overfitting.

Model_2 is a Multiple Linear Regression Model with 1850 Features created using feature engineering techniques such as
Polynomial Features for numeric variables and one hot encoding for nominal variables. All original features were also
considered while modeling. Model_2 responded better to the Lasso Regularization as it had an extensive list of features
and was the best performing model on Kaggle between the two created.

### Next Steps and Model Improvement:
- External Input to the Model
- New Imputation Techniques for Null Values
- Better Outlier Analysis
- Feature Selection Through Lasso and Implementation Through Ridge
- Implementation of GridScaler
