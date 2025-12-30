# CUSTOMER TRANSACTION PREDICTION

![Customer Transaction Prediction](CustomerTransaction.png)

## INTRODUCTION:
With the problem of predicting which customers will make a transaction with the bank in future,
irrespective of the amount of money transacted previously with the bank, the dataset contains
200000 observations with 202 columns. Out of these, 200 columns represent features named from
var_1 to var_200, one column represents the ID code, and one column represents the target variable.

## BUSINESS CASE:
Based on the given customer features, the objective is to predict whether a customer will make a transaction in the future.

## TASK:
BINARY CLASSIFICATION

NOTE:
* In this data we not do any domain analysis and eda because the data is contain private information of bank customer.
* In this data we only check the distribution of feature and target column.

## DOMAIN ANALYSIS AND EDA:
#### TARGET COLUMN == TARGET [0, 1]

* 0 Represent -- CUSTOMER DID NOT DO A TRANSACTION
* 1 Represent -- CUSTOMER DID DO THE TRANSACTION
#### OBSERVATION:
• In this plot we are clearly seen the 90% customer are did not do a transaction and 10% customer are did do the transaction  
• This target feature is imbalance so we need to balance the data with the help of oversampling.

## DATA PREPROCESSING AND FEATURE ENGINEERING:

1. MISSING VALUE:  
In this data no missing value is present.

2. CATEGORICAL DATA:  
This data is not contain any categorical feature.

3. OUTLIER HANDLING:  
In this data outlier is present in all feature, but we not handle outlier because the from above EDA part we understand the all feature is very close to the normal distribution and distance between two point is very less so we use robust scaling.

4. FEATURE SCALING:  
Here we are use Robust scalar to scale the feature between IQR, Because the all feature contain outlier and close to the normal distribution

## FEATURE SELECTION:

1. DROP UNIQUE AND CONSTANT COLUMN:  
In this data only one unique column is present

2. CHECK THE CORRELATION:  
In this data no highly correlated feature is present

3. CHECK DUPLICATES:  
There is no duplicates present in data

4. PRINCIPLE COMPONENT ANALYSIS:  
In PCA we are select 175 feature because the less variance loss

## MODEL CREATION AND SELECTION:

#### OBSERVATION:
• logistic regression model training and testing score is not good after applying bagging score is still lagging.

• ANN MLP Classifier model is very well work on training data as well as testing data the score of training is 93.87 and testing score is 90.47 with f1 score is 90.58

• XGBClassifier model give better performance than other model with training accuracy is 93.77 and testing accuracy is 90.60 with f1 score is 90.55

• Random Forest classifier also perform well but slightly lower than XGBClassifier model.

• From all the above models ANN MLP Classifier and XGBClassifier gives the best performance compared to other models.

## Dataset
The dataset used in this project is large and is not included in the repository. It can be obtained from the original source.





