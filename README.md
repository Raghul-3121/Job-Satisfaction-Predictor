# Predicting Job Satisfaction: A Data Science Case Study

## Introduction
Job satisfaction is a critical measure for organizational success. Understanding what drives employee happiness can help companies retain top talent and improve workplace productivity. This project explores how machine learning can predict job satisfaction based on multiple factors.

## Project Goals
- Predict employee job satisfaction (scale: 1-10) using features like salary, work-life balance, education, and experience.  
- Provide actionable insights for decision-makers via a visualization.  
- Overcome real-world challenges such as data imbalance, feature selection, and model interpretability.

## The Dataset

### Summary:
- **Records**: 38,444 employees.
- **Columns**: Field of Study, Current Occupation, Years of Experience, Education Level, Salary, Job Satisfaction (target), Work-Life Balance.

### Challenges Identified:
1. **Categorical Features**: Columns like `Field of Study` and `Current Occupation` were categorical, requiring encoding.
2. **Range of Scales**: Numerical features like `Years of Experience` and `Salary` were on different scales.
3. **Skewed Distributions**: Work-Life Balance and Job Satisfaction showed uneven distributions.

## Step-by-Step Process

### 1. Data Preprocessing

The first step was cleaning and preparing the dataset:
- **Encoding Categorical Variables**: Used `OneHotEncoding` for multi-class categories.
- **Scaling Numerical Features**: Standardized `Salary` and `Years of Experience` for uniformity.
- **Addressing Imbalance**: Ensured training and test splits reflected real-world distributions.

### 2. Feature Engineering

To extract deeper insights, I:
- **Created Interaction Features**: Explored combinations like `Salary x Work-Life Balance`.
- **Feature Selection**: Applied `Random Forest Feature Importance` to rank and select meaningful features.

### 3. Model Building and Evaluation

I chose **Random Forest Regressor** for its balance of performance and interpretability:
- **Hyperparameter Tuning**: Used `GridSearchCV` to optimize parameters like the number of trees and max depth.
- **Evaluation Metrics**:
  - **R² Score**: 0.87
  - **MSE**: 0.0126
  - **MAE**: 0.067

## Challenges & How I Overcame Them

1. **Imbalanced Data**: Resolved with careful train-test splits and resampling techniques.
2. **Feature Explosion**: Used feature selection to eliminate redundant features.
3. **Model Interpretability**: Focused on simple, explainable models for actionable insights.

## Key Insights

1. **Salary and Work-Life Balance** were the most influential features.
2. Employees with better work-life balance consistently reported higher satisfaction.
3. Education level played a lesser role than expected, highlighting the importance of organizational culture.

## Final Thoughts

This project was a fantastic learning experience, blending technical skills with real-world problem-solving. It taught me:
- The importance of starting with clean, well-understood data.
- How small mistakes can cascade but also provide learning opportunities.
- The value of storytelling in data science, from raw numbers to actionable insights.

## What’s Next?
- Deploying the model for real-time predictions.
- Expanding the dashboard’s capabilities to include interactive filters.
- Applying similar approaches to other HR datasets to explore broader trends.

## Let’s Connect!

If you’re interested in similar projects or have feedback, feel free to reach out! Check out the code, visuals, and dashboard screenshots in the repository.

[View Full Project on GitHub](Insert GitHub Link)
