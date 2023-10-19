# IndustrialAssetCare
Use machine learning to predict industrial machine failures. Code and resources for Random Forest-based models. Achieved F1 score ~0.674. Reduce downtime and costs.


Introduction
Predictive maintenance has become a crucial part of modern industrial operations. By leveraging machine learning techniques, we can create models that accurately predict machine failures before they occur, thereby reducing downtime and operational costs. In this guide, we delve into a data-driven approach to predict machine failures in an industrial setup. The analysis covers the entire data science pipeline—starting from data exploration to model evaluation.

Summary
We employed machine learning techniques, particularly the Random Forest Classifier, to predict machine failures. The dataset comprised several features like air and process temperature, rotational speed, torque, and tool wear. After data preprocessing and feature engineering, we developed an initial Random Forest model, which we later optimized using hyperparameter tuning. The optimized model showed promising results, with an F1 score of approximately 0.674.



Step-by-Step Guide

Data Exploration
Import Libraries and Data: Import essential Python libraries and read the CSV dataset.
Initial Look: Use df.head() to get an initial sense of the dataset.
Normalization: Normalize numerical columns using MinMaxScaler.
Data Preprocessing
Scaling: Scale the numerical columns again using MinMaxScaler.
Feature Engineering
Lag Features: Generate lag features for 'Air temperature [K]' and 'Torque [Nm]' for 1 and 2 time steps.
Drop NaN: Remove rows with NaN values.
Model Development
Train-Test Split: Perform a 70-30 time-based split on the dataset.
Initialize and Train Model: Initialize a RandomForestClassifier and fit it on the training data.
Model Evaluation
Metrics Calculation: Calculate Accuracy, Precision, Recall, and F1 score for the initial model.
Hyperparameter Tuning
RandomizedSearchCV: Use RandomizedSearchCV to find the best hyperparameters for the Random Forest model.
Optimized Model
Train Optimized Model: Train the Random Forest model using the optimized hyperparameters.
Evaluate Optimized Model: Calculate the performance metrics for the optimized model.
Interpretation of Results
The optimized model showed an F1 score of approximately 0.674, which is an improvement over the initial model. This indicates that the model is fairly good at predicting machine failures.

Feature Importances:
Torque [Nm]: 29.3% - The torque has the highest influence on machine failure.
Rotational speed [rpm]: 22.2% - Rotational speed is the second most crucial factor.
Process temperature [K]: 12.5% - Process temperature also plays a significant role.
The lag features we engineered also contributed to the model, albeit less significantly than the original features.

In conclusion, predictive maintenance using machine learning techniques like Random Forest can be highly effective. Our analysis shows that we can accurately predict machine failures, thus allowing ample time for preventive actions.
