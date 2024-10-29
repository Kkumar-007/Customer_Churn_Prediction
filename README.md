# Customer Churn Prediction Pipeline
This project is an end-to-end pipeline for predicting customer churn using machine learning. It includes loading, cleaning, and balancing data, training multiple models, hyperparameter tuning, and deploying the model for inference through a Streamlit app. Additionally, the model generates personalized emails to retain customers based on their churn probability.

## Project Overview
Customer churn prediction helps identify customers likely to leave a service, enabling targeted retention efforts. This project specifically considers that retaining a customer is more cost-effective than acquiring a new one, and the prediction model focuses on accuracy in identifying potential churners. The pipeline is built with a focus on high recall for reliable identification.

## Features
Data Preparation: Loading and cleaning the dataset, with handling of skewed data using SMOTE (Synthetic Minority Oversampling Technique) to achieve balanced classes.
Model Training: Training five different machine learning models:
Random Forest
XGBoost
K-Nearest Neighbors (KNN)
Support Vector Machines (SVM)
Decision Tree
Ensemble Voting: A majority voting mechanism is used to combine the results from three models and determine an average churn probability.
Key Factor Analysis: Trend analysis for customer churn and identification of influential factors to improve interpretability.
Evaluation Metrics: Recall is used as the primary evaluation metric, given that capturing potential churn is critical to this business application.
Visualization: Churn probabilities and contributing factors are presented graphically in the Streamlit web app for user-friendly insights.
Customer Retention Strategy: Llama-3.1 7B model generates custom emails offering incentives to high-risk customers to improve retention rates.

## Project Pipeline
Data Loading: Import the customer dataset and perform initial exploration.
Data Cleaning and Preprocessing: Handle missing values, outliers, and normalize/standardize features as needed.
Data Balancing: Apply SMOTE to balance the classes due to the high imbalance in churn and non-churn classes.
Feature Selection: Identify key features that most influence customer churn for focused insights and interpretability.
Model Training: Train and optimize five different machine learning models.
Hyperparameter Tuning: Tune model parameters using techniques like grid search to enhance model performance.
Model Evaluation: Evaluate the models based on recall to prioritize capturing potential churners accurately.
Ensemble Voting: Calculate an average churn probability using an ensemble voting approach from three selected models.
Deployment: Serve the model through a Streamlit app, allowing for real-time churn probability predictions and visualizations.
Customer Retention Email: Generate a personalized email for customers at high churn risk, offering tailored incentives to encourage retention.
