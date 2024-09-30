# DSN-2024-AI-BOOTCAMP-QUALIFICATION-HACKATHON
# Heart-Disease-prediction
## Introduction
The challenge at hand revolves around the creation of a sophisticated predictive model aimed at determining the likelihood of an individual having heart disease. As one of the leading causes of global mortality, detecting heart disease in its early stages is pivotal for enhancing patient outcomes and halting its progression. The conventional diagnostic methods often come with substantial costs and time requirements. Thus, there exists a pressing need for a cutting-edge predictive model that can evaluate the risk of heart disease utilizing easily accessible patient information.

The objective of this challenge is to design and build a predictive model capable of accurately determining the probability of an individual having heart disease. The focus is on leveraging machine learning techniques to create a model that can analyze relevant features and provide reliable predictions. The model should demonstrate high accuracy and generalizability, ensuring its effectiveness on new, unseen data.

## Problem Statement
The project focuses on how Early prediction aids in timely intervention and prevention, optimizing healthcare resources. The cost-effectiveness of predictive models reduces unnecessary procedures, benefiting patients and healthcare systems.. It harnesses the combined the application of: 
+ Features Engineering using log tranform, MinMaxScaler
+ Features Engineering MinMaxScaler
+ Cross-validation.

This project involved an in-depth understanding of the dataset provided which invloved the domain-level understanding of the features and their relationships. Data preprocessing began by checking for  missing values in the train dataset and applying features engineering to harness the relationship between the features. .

## Solution Overview

### Data preparation & preprocessing
The dataset was taken through several techniques starting from the the checking of missing values within the dataset. Next, the dataset contained no missing  values.

### Data visualization
 Data visualization was carried out on the data to understand the distribution of features as well as the target variable 

### Features Engineering
##Log Transform a logarithmic transformation technique was applied to features to reduce skewness in data.

train_l["trestbps_log"]=np.log(train_l["trestbps"])
test_l["trestbps_log"]=np.log(test_l["trestbps"])

##The MinMaxScaler was used to scale and normalize features by rescaling the values to be within a specified range
test_l["thalach_m"]=scaler.fit_transform(test_l[["thalach"]])
test_l["age_m"]=scaler.fit_transform(test_l[["age"]])

train_l["thalach_m"]=scaler.fit_transform(train_l[["thalach"]])
train_l["Age_m"]=scaler.fit_transform(train_l[["Age"]])
The arithmetic operations above were performed to create new features.

### Model Trainig, Validation and Evaluation
The logistic Regressoion algorithm was used to build a classification model with KFold cross-validation for the model validation. The Coefficient_attributes was checked and the exang , cp, and trestbps_log features had the highest feature importance 


## Features
The key features and functionalities used in this solution include:
+ Feature Engineering 
+ Setting the right hyperparameter for the model

## Technologies Used
+ Python programming language
+ Pandas
+ Scikit-learn
+ Randoom forest
+ Jupyter notebook

### Result
The model performed on an accuracy score of  0.8302532511978097

