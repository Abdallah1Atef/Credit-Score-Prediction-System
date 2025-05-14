# Credit Score Prediction System

![Credit Score Prediction](https://img.shields.io/badge/Python-3.8%2B-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.22.0-red)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.2.2-orange)

A machine learning pipeline for credit score classification using SVM models, deployed via Streamlit.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Data Pipeline](#data-pipeline)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Model Performance](#model-performance)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project implements a credit score prediction system that classifies customers into three categories:
- **Good**: Excellent creditworthiness
- **Standard**: Average creditworthiness
- **Poor**: High-risk credit profile

The system uses a sophisticated data preprocessing pipeline and SVM models with hyperparameter tuning through GridSearchCV.

## Features

- **Comprehensive Data Preprocessing**:
  - Handles missing values, outliers, and data inconsistencies
  - Specialized transformers for credit history age conversion
  - Advanced categorical encoding (ordinal + one-hot)
  
- **Model Training**:
  - SVM classifier with PCA dimensionality reduction
  - GridSearchCV for hyperparameter optimization
  - Feature selection based on ANOVA and correlation analysis

- **Streamlit Web App**:
  - Single prediction interface with form inputs
  - Batch prediction via CSV upload
  - Interactive visualization of results
  - Credit improvement tips
    
The app will launch in your default browser at http://localhost:8501

Using the Prediction System
Single Prediction:

Fill out the form in the sidebar

Click "Predict Credit Score"

View the prediction and probabilities

Batch Prediction:

Upload a CSV file with customer data

Download the predictions as CSV

Data Pipeline
The preprocessing pipeline includes these key transformations:

Credit History Age Conversion:

Converts strings like "5 Years and 3 Months" to total months

Numeric Cleaning:

Removes special characters from numeric fields

Handles outliers using IQR method

Categorical Processing:

Standardizes category strings

Imputes missing values using group modes

Mixed encoding (ordinal + one-hot)

Feature Selection:

Selects top features based on ANOVA F-values

Removes highly correlated features

Scaling & Dimensionality Reduction:

StandardScaler for normalization

PCA for feature reduction

Exploratory Data Analysis
Key insights from the EDA:

Class Distribution:

Standard: 53.2%

Poor: 31.4%

Good: 15.4%

Important Correlations:

Credit_History_Age ↔ Credit_Score (0.37)

Interest_Rate ↔ Credit_Score (-0.48)

Outstanding_Debt ↔ Credit_Score (-0.39)

Visualizations:

Distribution plots for all numeric features

Correlation heatmap

Boxplots showing relationships between features and credit score


## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/credit-score-prediction.git
   cd credit-score-prediction
