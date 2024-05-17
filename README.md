# Road-Traffic-Severity-Classification

## Overview
This project aims to predict the severity of road accidents based on various factors such as time, day of the week, driver details, vehicle information, road conditions, and more. The dataset used contains 12,316 rows and 12 columns.

## Dataset Details
- The dataset contains details about:
  - Time
  - Day of the week
  - Age band of driver
  - Sex of driver
  - Educational level
  - Vehicle-driver relation
  - Driving experience
  - Type of vehicle
  - Owner of vehicle
  - Service year of vehicle
  - Defect of vehicle
  - Area accident occurred
- The target variable is accident severity.

## Data Preprocessing
- Missing values and outliers were treated.
- Categorical variables were encoded to numerical.
- Class imbalance was handled using SMOTE.

## EDA Observations
- Most accidents involved 2 vehicles and 2 casualties.
- Accidents mostly occurred on Fridays and after noon hours.
- Most drivers were male, aged 18-30 years, with junior high school education, employees, and had 5-10 years of driving experience.
- Accidents primarily happened with personally owned passenger vehicles.
- The majority of accidents occurred between 3pm to 6pm, with the peak at 5pm.
- Time in minutes was recorded in intervals of 5 minutes for convenience, leading to more numbers at 0 and 30 minutes.

## Important Features Identified by Extremely Randomized Trees
After training the Extremely Randomized Trees model, the following features were identified as important for predicting accident severity:

- Number of vehicles involved
- Number of casualties
- Light conditions
- Driver age
- Day of the week
- Minute of the accident
- Road surface conditions
- Driving experience of the driver
- Type of junction
- Hour of the accident

## Model Selection and Performance
- Various machine learning algorithms were experimented with.
- Extremely Randomized Trees outperformed other algorithms with an accuracy of 0.8.
- Hyperparameters for Extremely Randomized Trees:
  - `max_depth`: None
  - `max_features`: 'sqrt'
  - `max_leaf_nodes`: None
  - `max_samples`: None

## Hyperparameter Tuning
- Grid search was used for hyperparameter tuning.

## Dependencies
- Python 3.x
- scikit-learn
- pandas
- numpy
