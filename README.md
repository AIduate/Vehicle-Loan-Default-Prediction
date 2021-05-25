# Vehicle-Loan-Default-Prediction

## Table of contents
* [Introduction](#introduction)
* [Sources](#sources)
* [Technologies](#technologies)
* [Libraries](#libraries)
* [Files](#files)
* [Results](#results)

## Introduction 
The objective of this project is to derive insights on attributes related to vehicle loan defaulting and build an initial predictive model & pipeline.

## Sources
https://www.kaggle.com/mamtadhaker/lt-vehicle-loan-default-prediction?select=data_dictionary.csv

## Technologies
Python 3.6

## Libraries
```
import pandas as pd

from sklearn.preprocessing import OneHotEncoder

import numpy as np

from sklearn.model_selection import train_test_split

from sklearn.linear_model import LogisticRegression

import sklearn.metrics as metrics

import seaborn as sn

import matplotlib.pyplot as plt
```

## Files
data_dictionary.csv - text file containing column names and descriptions

train.csv - text file containing columns described in data_dictionary.csv

test.csv - text file containing columns described in data_dictionary.csv without target variable: loan_default

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

Decision threshold was adjusted to 0.3 to increase performance to resulting ROC AUC of: 0.5193696057892393

Current takeaways:
- Loanees with high, very high, medium and no bureau history available with longer credit history are slightly less likely to default their loans
- it seems those with lower bureau scores (that have been scored) and defaulted their loans, tend to have more inquiries
- The top 5 most influential attributes associated with vehicle loan defaults are 'PERFORM_CNS.SCORE', 'asset_cost', ltv', 'CREDIT.HISTORY.LENGTH.MONTHS', and 'PRI.Installment.PCT'

