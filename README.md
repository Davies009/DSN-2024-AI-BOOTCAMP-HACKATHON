# DSN-2024-AI-BOOTCAMP-QUALIFICATION-HACKATHON
# Heart-Disease-prediction
## Introduction
The challenge at hand revolves around the creation of a sophisticated predictive model aimed at determining the likelihood of an individual having heart disease. As one of the leading causes of global mortality, detecting heart disease in its early stages is pivotal for enhancing patient outcomes and halting its progression. The conventional diagnostic methods often come with substantial costs and time requirements. Thus, there exists a pressing need for a cutting-edge predictive model that can evaluate the risk of heart disease utilizing easily accessible patient information.

The objective of this challenge is to design and build a predictive model capable of accurately determining the probability of an individual having heart disease. The focus is on leveraging machine learning techniques to create a model that can analyze relevant features and provide reliable predictions. The model should demonstrate high accuracy and generalizability, ensuring its effectiveness on new, unseen data.

## Problem Statement
The project is aimed at using historical housing data in Nigeria to predict the price of houses in different states. It harnesses the combined the application of: 
+ Features Engineering using Arithmetic operations,  Geographical classification, Ranking
+ Features Encoding using Target encoding
+ Cross-validation.

This project involved an in-depth understanding of the dataset provided which invloved the domain-level understanding of the features and their relationships. Data preprocessing began by filling in the missing values in the train dataset and  applying features engineering to harness the relationship between the features. Other techniques like ranking, and geographical classification were employed to the features. 
## Solution Overview
### Data preparation & preprocessing
The dataset was taken through several techniques starting from the the filling of missing values with the median due to outliers in the dataset. Next, the missing values in the categorical features were dropped.

### Features Engineering
Log Transform a logarithmic transformation technique was applied to features to reduce skewness in data ().
data['room_conv'] = data['bedroom'] / data['bathroom']

data['size'] = data['bedroom'] + data['bathroom'] + data['parking_space']
    
data['occup'] = data['bedroom'] / data['parking_space']. 

The arithmetic operations above were performed to create new features. The house titles were ranked according to their importance and the state feature were aggregated into geographical area.
### Data Encoding
Target encoding was performed on the categorical features: Location and Title

### Model Trainig, Validation and Evaluation
The Catboost Regressor algorithm was used to build a regression model with KFold cross-validation for the model validation. The feature importance was checked and the location, title, and bedroom features had the highest feature importance score.

Loc:  28.018083350237955

new_title: 20.514683864991927

bedroom: 19.554140457133617

## Features
The key features and functionalities used in this solution include:
+ Feature Engineering 
+ Setting the right number of splits

## Technologies Used
+ Python programming language
+ Pandas
+ Scikit-learn
+ Randoom forest
+ Jupyter notebook

### Result
The model performed a 326440.862 RMSE score on the public leader board and 326440.862 RMSE score on the private leaderboard. This result placed me 5th postion on the leaderboard.

