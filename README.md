# Vehicle-Loan-Default-Prediction

## Table of contents
* [Introduction](#introduction)
* [Acknowledgements](#acknowledgements)
* [Technologies](#technologies)
* [Libraries](#libraries)
* [Files](#files)
* [Results](#results)

## Introduction 
The objective of this project is to derive insights on attributes related to vehicle loan defaulting and build an initial predictive model & pipeline.

Early questions of interest to investigate:
* What are the most influential attributes associated with vehicle loan defaults?
* If someone has been shopping around for loans, what is the relationship between number of loan inquiries and potential to default the loan?
* How does credit history age affect risk to default?

## Acknowledgements
Data with sourced from Kaggle: https://www.kaggle.com/mamtadhaker/lt-vehicle-loan-default-prediction?select=data_dictionary.csv.
This link also includes a helpful description & business context.

## Technologies
Python 3.6

## Libraries

* pandas
* sklearn
* numpy
* seaborn 
* matplotlib

## Files
* data_dictionary.csv - text file containing column names and descriptions
* train.csv - text file containing columns described in data_dictionary.csv
* test.csv - text file containing columns described in data_dictionary.csv without target variable: loan_default

## Results

A preliminary logistic regression model was trained on the following features:
* 'AVERAGE.ACCT.AGE.MONTHS'
* 'Aadhar_flag'
* 'AgeAtDisbursal'
* 'CREDIT.HISTORY.LENGTH.MONTHS'
* 'DELINQUENT.ACCTS.IN.LAST.SIX.MONTHS'
* 'DisbursalMonth'
* 'DisbursalWeekday'
* 'Driving_flag'
* 'MobileNo_Avl_Flag'
* 'NEW.ACCTS.IN.LAST.SIX.MONTHS'
* 'NO.OF_INQUIRIES'
* 'PAN_flag'
* 'PERFORM_CNS.SCORE'
* 'PRI.ACTIVE.ACCTS'
* 'PRI.CURRENT.BALANCE'
* 'PRI.DISBURSED.AMOUNT'
* 'PRI.Installment.PCT'
* 'PRI.NO.OF.ACCTS'
* 'PRI.OVERDUE.ACCTS'
* 'PRI.SANCTIONED.AMOUNT'
* 'PRIMARY.INSTAL.AMT'
* 'Passport_flag'
* 'SEC.ACTIVE.ACCTS'
* 'SEC.CURRENT.BALANCE'
* 'SEC.DISBURSED.AMOUNT'
* 'SEC.INSTAL.AMT'
* 'SEC.Installment.PCT'
* 'SEC.NO.OF.ACCTS'
* 'SEC.OVERDUE.ACCTS'
* 'SEC.SANCTIONED.AMOUNT'
* 'VoterID_flag'
* 'asset_cost'
* 'disbursed_amount'
* 'ltv'
* 'Employment.Type (values one hot encoded)
* 'manufacturer_id (values one hot encoded)
* 'PERFORM_CNS.SCORE.DESCRIPTION (values one hot encoded)
* 'State_ID (values one hot encoded)

Decision threshold was adjusted to 0.25 to increase performance to resulting  
ROC AUC of: 0.5307070727456186, f1 score of 0.3227277168072426 and confusion matrix:

                 actual neg   actual pos 

      pred pos     15630   |    4955    |

      pred neg     20879   |    5167    |


***Current takeaways:***

**What are the most influential attributes associated with vehicle loan defaults?**

- The top 5 most influential attributes associated with vehicle loan defaults based on my analysis so far are  
asset_cost, disbursed_amount, PERFORM_CNS.SCORE, SEC.SANTIONED_AMOUNT, and PRI.DISBURSED.AMOUNT.

**If someone has been shopping around for loans, what is the relationship between number of loan inquiries and potential to default the loan?**
 
- It seems those with lower bureau scores (that have been scored) and defaulted their loans, do tend to have more inquiries.

**How does credit history age affect risk to default?**

- Loanees with high, very high, medium and no bureau history available with longer credit history are slightly less likely to default their loans based on my analysis so far.

See the corresponding blog post for this project at: https://aiduate.medium.com/what-lies-in-the-road-ahead-9de3f04d2508

