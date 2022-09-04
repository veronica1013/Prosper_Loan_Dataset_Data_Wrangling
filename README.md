# Prosper_Loan_Dataset_Data_Wrangling
## 1. Dataset

1.0 Introduction

The dataset that will be used for this project is available via [this url](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv). It entails loan details of customers entailing their loan status, credit grade, loan term etc.

**1.1.0 Main Objective**

The main aim of this project is to identify what factors affect a loan’s outcome status.

**1.1.1 Specific Objectives**
>* To find out what affects the borrower’s APR or interest rate.
>* To identify if there are differences between loans depending on how large the original loan amount was.

**1.2.2 The structure of the dataset**

The data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.

**1.2.2.1 The main feature(s) of interest in the dataset.**

Since I'll be focusing on the features that affect the loan status, the main features that will help in looking at the relationship they have with the loan status are:

* a. CreditGrade,
* b. Term,
* c. ProsperRating (Alpha),
* d. 'ProsperScore',
* e. ListingCategory (numeric),
* f. Occupation,
* g. EmploymentStatus,
* h. EmploymentStatusDuration,

**1.2.2.2 The features in the dataset that will help support the investigation into the feature(s) of interest are:**
* a. 'BorrowersState',
* b. 'IsBorrowerHomeowner',
* c. 'CurrentlyInGroup',
* d. 'DateCreditPulled',
* e. 'CreditScoreRangeLower',
* f. 'FirstRecordedCreditLine',
* g. 'CurrentCreditLines',
* h. 'OpenCreditLines',
* i. 'TotalCreditLinespast7years',
* j. 'OpenRevolvingAccounts',
* k. 'OpenRevolvingMonthlyPayment',
* l. 'CurrentDelinquencies',
* m. 'AmountDelinquent',
* n. 'DelinquenciesLast7Years',
* o. 'RevolvingCreditBalance',
* p. 'TotalTrades',
* q. 'TradesNeverDelinquent (percentage)',
* r. 'TradesOpenedLast6Months',
* s. 'DebtToIncomeRatio',
* t. 'IncomeRange',
* u. 'StatedMonthlyIncome',
* v. 'LoanCurrentDaysDelinquent',
* w. 'Recommendations'

## 2.0  Data Wrangling Steps
There were missing values which I imputed them with the mean for the numeric features. I performed feature engineering on the Employment Status Duration as this was in months which was divied by 12 to convert it to number of years. This helped in proper visualization of the histogram. On the visualization stage, I performed univariate, bivariate and multivariate analysis. 

On univariate analysis, I plotted bar charts and histograms for the categorical and numerical features. For categorical features, I plotted bar charts and histograms for numerical features. During multivariate analysis, I looked at the relationship between loan status and each of the other features. I plotted grouped bar charts, point plot, scatter plots and histograms using facetgrid. I adjusted the yticks where there were values like 50000 to 50k. I also used resized the bins to plot accurate range of data points. For ordinal data, I ordered them by setting the to astype category before visualizing. 


## 3.0 Summary of Findings

>It was noted that borrowers who had less repayment term period of 12 months were able to complete their loan payments. majority of those who had high prosper score and recommendations scores had current loans and others completed paying their loans. High income earners with income range of above 100,000 dollars secured loans with long term period. 

> Borrowers who had a high number of open and current revolving accounts had current loans or completed paying their loans. Most borrowers took loans for home improvement which was category one on the listing category. It was also evident form the count plot that majority of the home owners took loans.

> Borrowers with a long term payment period 36 and 60 months were the majority of defaulters while those with short term repayment period of 12 months were able to repay their loans.

> There was a link on the income debt ration to loan status. The borrowers with high debt to income ratio defaulted their loans and also had most of their loans in past due. I also noted that the borrowers with loans that had high borrowers rate defaulted their loans.

> When considering to give a loan, the features for consideration are:
a. Income to debt ratio,
b. Revolving Accounts
c. Current Revolving Accounts
d. Total Trades
e. Term Duration
f. Recommendation Scores
g. Prosper Scores
h. Monthly Revolving Amounts
i. Borrowers Rate


## 4.0 Key Insights for Presentation

> For the exploration, I narrowed down to visualizing a swarm plot for borrower state, prosper score and term. It was evident that majority of the borrowers from all he state covered considered short term loans of 12 months and they all had a high prosper score compared to the loan term of 36 and 60 months.
