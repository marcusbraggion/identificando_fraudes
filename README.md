[
![1_xSqK9iS7nZAaB-Sdwiwjow](https://user-images.githubusercontent.com/97288194/150184248-349f43ea-c929-416d-8a2c-53b821eff9a6.png)
](url)

# Ieee-CIS-Fraud Detection

# 1.0 Business Context (Fictitious)
IEEE CIS is a company specialized in detecting fraud in financial transactions through mobile devices. The company has a service called “Blocker Fraud” with no guarantee of blocking fraudulent transactions.

And the company's business model is of the service type with monetization made by the provider's performance, that is, the user pays a fixed fee on the success in the fraud detection of the customer's transactions.

# 2.0 Challenge

The CFO want to improve the efficacy of fraudulent transaction alerts, helping hundreds of thousands of businesses reduce their fraud loss and increase their revenue.

# 3.0 Business Assumptions

The data is broken into two files identity and transaction, which are joined by TransactionID. Not all transactions have corresponding identity information.

Categorical Features - Transaction

ProductCD

card1 - card6

addr1, addr2

P_emaildomain

R_emaildomain

M1 - M9

Categorical Features - Identity

DeviceType

DeviceInfo

id_12 - id_38

The TransactionDT feature is a timedelta from a given reference datetime (not an actual timestamp).

# 4.0 Solution Strategy

The strategy adopted was the following:

**Step 01.** Data Description: I searched for NAs, checked data types (and adapted some of them for analysis) and presented a statistical description.

**Step 02.** Feature Engineering: New features were created to make possible a more thorough analysis.

**Step 03.** Data Filtering: Entries containing no information or containing information which does not match the scope of the project were filtered out.

**Step 04.** Exploratory Data Analysis: I performed univariate, bivariate and multivariate data analysis, obtaining statistical properties of each of them, correlations and testing hypothesis (the most important of them are detailed in the following section).

**Step 05.**. Data Preparation: Here I chose to use LabelEncoder method for  categorical features.

**Step 06.** Feature selection: The statistically most relevant features were selected using the Boruta package. Alternatively, I performed the feature selection using the Random Forest as feature selector, obtaining the "feature importances" from both of them. In the next steps, the machine learning models trained using the features selected by Boruta presented a better generalizability performance.

**Step 07.** Machine learning modelling: Some machine learning models were trained. The one that presented best results after cross-validation went through a further stage of hyperparameter fine tunning to optimize the model's generalizability.

**Step 08.** Model-to-business: The models performance is converted into business values.

# 5.0 Conclusions
I used the LGBM Classifier model to learn all the behavior of the data, and after modeling the data, I used it to make predictions, using a sample of 20% of complete data set to avoid memory error. After that, I splited it in 70% of the dataset to train it and then test it on 30% of the data not seen by the model to measure its performance. After all the steps mentioned and with the predictions made, I performed the evaluation of the model's performance, bringing the result of the classification for each transaction, through four metrics: precision, accuracy, recall, f1-measure. I also brought 3 graphs that demonstrate the result and error of the model for transaction and finally I was able to generate a model result with a total saved loss of R$ 34.50,000 and 89% transaction fraud detection.

# 6.0 Next steps and Improvements
Increase model accuracy by 5%.
