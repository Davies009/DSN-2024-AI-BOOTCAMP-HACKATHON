# DSN-2024-AI-BOOTCAMP-QUALIFICATION-HACKATHON
# Heart Disease prediction
## Introduction
Wazobia Real Estate Limited is a prominent real estate company operating in Nigeria. With a vast portfolio of properties, they strive to provide accurate and competitive pricing for houses. However, they have been facing challenges in accurately predicting the prices of houses in the current market.
The objective of this project is to create a powerful and accurate predictive model that can estimate the prices of houses in Nigeria. By leveraging a comprehensive dataset, various factors that impact house prices, identify meaningful patterns are analyzed. he ultimate goal is to provide Wazobia Real Estate Limited with an effective tool to make informed pricing decisions and enhance their competitiveness in the market.
### N.B: This is a winning solution to the 2023 DSN & Microsoft Machine Learning hackathon.

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
+ Target Encoding
+ Feature Engineering 
+ Setting the right number of splits

## Technologies Used
+ Python programming language
+ 2 T4 NVIDIA GPUs
+ Pandas
+ Scikit-learn
+ Catboost
+ Kaggle Notebook Kernel

### Result
The model performed a 326440.862 RMSE score on the public leader board and 326440.862 RMSE score on the private leaderboard. This result placed me 5th postion on the leaderboard.

Link to the Leaderboard standings: https://zindi.africa/competitions/free-ai-classes-in-every-city-hackathon-2023/leaderboard
