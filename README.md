# Customer Churn Prediction Using Artificial Neural Networks

This project aims to predict customer churn using an Artificial Neural Network (ANN) model. Customer churn refers to when a customer discontinues using a product or service. Predicting churn can help businesses retain customers by targeting interventions at high-risk customers.
(https://customer-churn-prediction-using-ann-geography-h4dnbbejpssu3poo.streamlit.app/)

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview
Customer churn prediction is a key challenge for businesses. By identifying which customers are likely to churn, businesses can take proactive measures to retain those customers. This project uses an ANN to model customer churn behavior based on historical data.

## Dataset
The dataset used for this project is sourced from [Insert Source if applicable]. It contains the following features:
- `CreditScore`: Credit score of the customer
- `Geography`: Country of the customer
- `Gender`: Gender of the customer
- `Age`: Age of the customer
- `Tenure`: Number of years the customer has been with the bank
- `Balance`: Account balance
- `NumOfProducts`: Number of products the customer has with the bank
- `HasCrCard`: Whether the customer has a credit card
- `IsActiveMember`: Whether the customer is an active member
- `EstimatedSalary`: Estimated annual salary
- `Exited`: Target variable (1 if the customer churned, 0 if not)


Preprocessing steps are performed initially by remove unwanted columns and by converting the categorical columns into Numerical columns
The Geography column is converted using the OneHot Encoding and the Gender column is tranformed is==using the LabelEncoding technique

Inorder to check the dependencies, the correlation plot was plotted between the dependednt and independent feature. 
![image](https://github.com/user-attachments/assets/774793cd-463c-489a-b057-bdec35078fba)

## Model Architecture
The Artificial Neural Network (ANN) consists of:
- Input layer: Accepts all feature inputs
- Two hidden layers using ReLU activation
- Output layer using Sigmoid activation to predict the probability of churn
- Optimizer: Adam with a learning rate of 0.01
- Loss function: Binary Crossentropy

### Model Summary:
| Layer         | Type   | Output Shape | Param # |
|---------------|--------|--------------|---------|
| Hidden Layer 1| Dense  | (None, 64)   | 832     |
| Hidden Layer 2| Dense  | (None, 32)   | 2080    |
| Output Layer  | Dense  | (None, 1)    | 33      |
| **Total**     | -      | -            | 2945    |


