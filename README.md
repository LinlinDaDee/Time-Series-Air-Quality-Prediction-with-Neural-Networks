# Time Series Air Quality Prediction with Neural Networks

## Project Overview

This project involves developing neural network models for time series air quality prediction, focusing on two main tasks: classification and regression. The dataset used is the “Air Quality” dataset from the UCI Machine Learning Repository, which contains hourly averaged responses from an array of metal oxide chemical sensors embedded in an air quality chemical multisensor device.

## Objectives

1. Classification Task: Develop a neural network to predict whether the concentration of Carbon Monoxide (CO) exceeds a certain threshold based on historical air quality data.
2. Regression Task: Develop a neural network to predict the concentration of Nitrogen Oxides (NOx) based on other air quality features.

## Dataset

The dataset contains 8,358 instances of hourly averaged responses from sensors located in a polluted area at road level within an Italian city. Data were recorded from March 2004 to February 2005. Variables in the dataset include:

- CO(GT): True hourly averaged concentration of carbon monoxide
- PT08.S1(CO): Hourly averaged sensor response
- NMHC(GT): True hourly averaged overall Non-Metanic HydroCarbons concentration
- C6H6(GT): True hourly averaged Benzene concentration
- PT08.S2(NMHC): Hourly averaged sensor response
- NOx(GT): True hourly averaged NOx concentration
- PT08.S3(NOx): Hourly averaged sensor response
- NO2(GT): True hourly averaged NO2 concentration
- PT08.S4(NO2): Hourly averaged sensor response
- PT08.S5(O3): Hourly averaged sensor response
- T: Temperature
- RH: Relative Humidity
- AH: Absolute Humidity

Missing values within the dataset are tagged with -200.

## Tasks

1. Classification Task
   - Objective: Predict whether the concentration of CO exceeds the mean value of CO(GT).
   - Steps:
     - Calculate the mean value of CO(GT) excluding missing values.
     - Handle missing values appropriately.
     - Develop a neural network model for binary classification.
     - Feature selection using correlation heatmap.
     - Save the model with the least val_loss as the final model.
     - Evaluate the model using accuracy, precision, and a confusion matrix.	

2. Regression Task
   - Objective: Predict the concentration of NOx based on other air quality features.
   - Steps:
     - Calculate the mean value of CO(GT) excluding missing values.
     - Handle missing values appropriately.
     - Develop a neural network model for regression.
     - Feature selection using correlation heatmap.
     - Save the model with the least val_loss as the final model.
     - Evaluate the model using RMSE, MAE.

## Key Outcomes
1. Classification Task: The neural network achieved an accuracy of 93% and a precision of 95% for predicting whether the CO concentration exceeds the mean value on the Generalization Dataset.
2. Regression Task: The neural network’s performance for predicting NOx concentrations is evaluated using RMSE and MAE, with RMSE of 124.45 and MAE of 83.36 on the Generalization Dataset.
