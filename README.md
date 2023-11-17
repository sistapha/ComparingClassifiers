
# Practical Application Assignment 17.1: Comparing Classifiers

GitHub Repository for work done on Professional Certificate in Machine Learning and Artificial Intelligence - Jul 2023

## Introduction
This repository contains the Jupyter Notebook for the Application Assignment 17.1. This takes a sample jupyter notebook to complete the exercise to analyse UCI Bank Marketing Data Set in bank-additional-full.csv file in the data folder of this repository to build a machine learning application that uses classifications to evaluate customers that will accept the Long-term deposit application using features like job, marital status, education, housing and personal loan.

The goal of this project is to compare the performance of the following classifiers namely

K Nearest Neighbor
Logistic Regression
Decision Trees and
Support Vector Machines

In comparing the models, the training times and accuracy of the models will be recorded. This should provide an indication on the model that will provide predictions to determine which customer will accept the long term deposit bank product via a phone based marketing campaign.
## How to use the files in this repository?

The notebooks are grouped into the following categories:

* articles – More information on the data and features
* data – vehicles.csv data file from Kaggle Machine Learning dataset repository used in the notebooks
* images – Image files used in Notebook and Project Description
* notebook – What Drives the Price of a Car Notebook
## Business Objective

The objective of this project is to find a model that can explain success of marketing programs run by a bank in driving customer subscriptions to deposit accounts. Such a model can be valuable in increasing campaign efficiency by identifying the key success drivers of a cmpaign, and can lead to a more efficient allocation of marketing resources while delivering a higher ROI on the deployed resources.

This is done by tryig out different classification models. Classification is a supervised machine learning method where the model tries to predict the correct label of a given input data. In classification, the model is fully trained using the training data, and then it is evaluated on test data before being used to perform prediction on new unseen data.
## Data Understanding

Goal here is to examine data, ensure it does not have missing values.

## Input variables
### Bank Client Data:
1 - age (numeric)
2 - job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
5 - default: has credit in default? (categorical: 'no','yes','unknown')
6 - housing: has housing loan? (categorical: 'no','yes','unknown')
7 - loan: has personal loan? (categorical: 'no','yes','unknown')
### related with the last contact of the current campaign:
8 - contact: contact communication type (categorical: 'cellular','telephone')
9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
10 - day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
### Other Attributes:
12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
14 - previous: number of contacts performed before this campaign and for this client (numeric)
15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')
### Socio economic Context Attributes
16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)
17 - cons.price.idx: consumer price index - monthly indicator (numeric)
18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)
19 - euribor3m: euribor 3 month rate - daily indicator (numeric)
20 - nr.employed: number of employees - quarterly indicator (numeric)

## Target variable:
21 - y - has the client subscribed a term deposit? (binary: 'yes','no')
## Data Preparation

The dataset was prepared for modeling as follows:

* Use features 1 - 7 (age, job, marital, education, default, housing, loan) to create a feature set
* Use ColumnTransformer to selectively apply data preparation transforms
* Use LabelEncoder to encode labels of the target column

With the data prepared, split it into a train and test set using the train_test_split function. We use 30% of the data as the test set.


## Baseline Model Comparison
