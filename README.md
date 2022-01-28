[
![1_xSqK9iS7nZAaB-Sdwiwjow](https://user-images.githubusercontent.com/97288194/150184248-349f43ea-c929-416d-8a2c-53b821eff9a6.png)
](url)

# IeeeCISFraud Detection

# 1.0 Business Context (Fictitious)
IEEE CIS is a company specialized in detecting fraud in financial transactions through mobile devices. The company has a service called “Blocker Fraud” with no guarantee of blocking fraudulent transactions.

And the company's business model is of the service type with monetization made by the provider's performance, that is, the user pays a fixed fee on the success in the fraud detection of the customer's transactions.

# 2.0 Business Problem
## 2.1 What is the context?
However, the IEEE CIS is in the expansion phase in Brazil and for customers more quickly,

## 2.2 What is the cause?
The CEO of IEEE CIS wants to improve the fraud detection rate and hire our expert data science consultancy to solve this problem.

## 2.3 Who will lead the project?
We need someone who really knows what the business problem is, because he's going to lead the solution. Therefore, he is our stakeholder.

## 2.4 What will our solution look like?
Predict the likelihood of an online transaction being fraudulent as indicated by the isFraud binary target using machine learning classification techniques.

# 2.0 Business Assumptions

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

# 3.0 Solution Strategy

**Step 01:**: Data Collection: Data was collect from https://www.kaggle.com/c/ieee-fraud-detection/overview

**Step 02:** Data Description

**Step 03:** Feature Engineering

**Step 04:** Exploratory Data Analysis

**Step 05:** Data Preparation

**Step 06:** Feature Selection

**Step 07:** ML Modeling

**Step 08:** Hyperparameters Fine Tuning

**Step 09:** Interpretação e Tradução do Erro

**Step 10:** Deploy Model to Production

# 4.0 Future Works and Learned Lessons
