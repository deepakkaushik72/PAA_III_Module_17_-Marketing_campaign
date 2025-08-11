# Practical Application Assignment III : Marketing Campaign Conversion Rate
## Link to Jupyter Notebook: https://github.com/deepakkaushik72/PAA_III_Module_17_-Marketing_campaign/blob/main/prompt_III.ipynb
## Link to Images: https://github.com/deepakkaushik72/PAA_III_Module_17_-Marketing_campaign/tree/main/Images%20-%20Analysis
## Link to Data: https://github.com/deepakkaushik72/PAA_III_Module_17_-Marketing_campaign/blob/main/bank-additional-full.csv

### 1. BUSINESS PROBLEM:
> - The business goal is to find a model that can predict in advance whether a customer will subscribe to a term deposit based on their demographic, history and social and economic attributes (21 Numerical and Categorical variables in Dataset)
> - Help the bank to target potential customers more effectively and improve their customer target effectiveness (Conversion Rate) and optimize the Return on Marketing     Investment (ROMI)
### 2. APPROACH
> - This is a binary classification problem where the target variable is 'y' which indicates whether the customer has subscribed to a term deposit or not (1 - Yes, 0 - No).
> - Will be using the Supervised Machine Learning Classification models.
> - The model will be trained on a dataset containing various features such as age, job, marital status, education, default status, housing loan status, personal loan status, contact communication type, last contact month of the year, number of contacts performed during this campaign, number of days since the customer was last contacted from a previous campaign, number of contacts performed before this campaign and the outcome of the previous marketing campaign.
> - Different classification models like Logistics Regression, Decision Tree, KNN and SVM will be used to predict the target variable
### 3. SUCCESS CRITERION:
> Deploy the model will predict whether a customer will Subscribe to Term Deposit or not with the following success criteria: 
> - Highest Recall of the positive class (y=1) while keeping accuracy over 80%
> - Maximizing the conversion rate (Precision) of the Marketing campaign and optimizing the Return on Marketing Investment
> - Optimizing the F1 Score (Precision-Recall Tradeoff)
### 4. DATA PREPARATION:
> - There are 41188 records in the file: “bank-additional-full.csv”
> - There are 12 duplicate records that have to be deleted
> - Imbalanced class distribution as there are only 12% in the positive class (only 12% of the total customers reached subscribed to the Term Deposit)
> - Looked at 21 features (10 numerical and 11 categorical including Target variable)
> - Job, Marital, education, default, housing, loan have “Unknown Values”, so these are missing values and hence dropped from the Dataset. Dropped 10,400+ records from the dataset. Final dataset/Data frame called “Bank” has only 30478 records  
> - Dropped the “Duration” column out from the final data frame as We will never know the duration before it happens
### 5. DATA UNDERSTANDING:
> - Most important Numerical features are:  'previous', 'pdays', 'emp.var.rate', 'euribor3m', 'nr.employed' and are negatively correlated to the conversion rate
> - Age, Campaign and Consumer confidence Index show extremely low correlation with the conversion rate.
> - Most important Categorical features are: Job', 'Education', 'Default', 'Month', 'Poutcome'
>> - "No Default" have a very significant impact on Conversion Rate
>> - "Student" and "Retired" have higher conversion rates (over 25%).
>> - "Illiterate" category have a higher conversion rate (over 25%) compared to other education levels
>> - "Sept, Oct, Dec and March" have over 40% conversion rates
>> - "Poutcome": Success of the previous campaign outcome leads to higher 
 conversion rates (over 60%
