# Mini-project IV

### [Assignment](assignment.md)

## Project/Goals
We want to automate the loan eligibility process based on customer details that are provided as online application forms are being filled. 
These details concern the customer's Gender, Marital Status, Education, Number of Dependents, Income, Loan Amount, Credit History and other things as well.
## Hypothesis
(fill in your hypothesis about which subset of applicants will be most likely to have their loan approved, and why. Give some examples of how you will test this hypothesis)
1. Applicants having a credit history
2. Applicants with higher applicant and co-applicant incomes
3. Applicants with higher education level
4. Properties in urban areas with high growth perspectives
## EDA 
The train set contains 614 rows and 13 columns of features. The features in the test set are similar to those in the train set.We need to predict the loan status using the model built on the train data. 

variables in different formats:

1. Object: Variables in object format are categorical variables. Examples of categorical variables in our dataset include Loan_ID, Gender, Married, Dependents, Education, Self_Employed, Property_Area, and Loan_Status.
2. Int64: Int64 format represents integer variables. An example of an integer variable in our dataset is ApplicantIncome.
3. Float64: Float64 format represents variables with decimal values, which are also numerical variables. Examples of numerical variables in our dataset include CoapplicantIncome, LoanAmount, Loan_Amount_Term, and Credit_History.


## Process

### Step 1 Data Exploration
 1. Data exploration  
 2. Address missing values
 4. Performed some basic statistics for numerical variables
 5. Measured the distribution of various variables using histogram & box plots
### Step 2 Data Cleaning
   This step typically involves imputing missing values and treating outliers.
   Imputing Missing Values using one hot encoding.
   Used a log transformation to get rid of the extreme values
### Step 3 Building a Predictive Model
  PCA shows Training accuracy: 0.6965376782077393
            Testing accuracy: 0.6504065040650406
  Logistic Regression shows Test accuracy: 0.7737837837837838
  paramater grid search was used to improve the results
  Best parameters:  {'max_depth': 40, 'min_samples_leaf': 20, 'min_samples_split': 18, 'n_estimators': 150} Best score was observed to be at 0.7785499316005472
### Step 4 Using Pipeline
Pipeline was created to take one row of the dataset and predict the probability of being granted a loan.
### Step 5 Deploying ML
Machine learning model was deployed using Flask

## Results/Demo
Initially, the Logistic Regression model achieved an accuracy of 78.378%. However, to further improve the results, a parameter grid search was performed. The grid Best parameters:  {'max_depth': 40, 'min_samples_leaf': 20, 'min_samples_split': 18, 'n_estimators': 150} Best score was observed to be at 0.7785499316005472

## Challanges 
The data set size was small and simple so would like to get more challenging and complex project. 

## Future Goals
Do some analysis with larger data set and check the accuracy of the model. Monitor the model, improve the result and tunning of parameters.