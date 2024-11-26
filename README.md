# Predicting Job Satisfaction: A Data Science Case Study

## Introduction

Job satisfaction is often overlooked, but it plays a vital role in an organization’s success. When employees are happy, productivity soars and retention improves. But what exactly drives job satisfaction? And can we predict it with data? In this case study, I dive into this question by applying machine learning to a dataset of employee characteristics and satisfaction levels. The goal? To predict how satisfied employees are and uncover the hidden factors behind their happiness.

## Project Goals

The aim of this project was clear:
- **Predict job satisfaction** (on a scale from 1 to 10) using factors like salary, work-life balance, education, and experience.
- **Provide insights for HR decision-makers** with visualizations to help them understand key drivers of job satisfaction.
- **Tackle real-world challenges** such as handling imbalanced data, feature selection, and building a model that's interpretable.

## The Dataset

The dataset at hand consisted of **38,444 records** of employees and included key features such as:
- **Field of Study**
- **Current Occupation**
- **Years of Experience**
- **Education Level**
- **Salary**
- **Work-Life Balance**
- **Job Satisfaction** (this is the target column)

However, with such a large dataset, I faced a few challenges that required thoughtful solutions:
1. **Categorical Features**: Some columns like `Field of Study` and `Current Occupation` were categorical, requiring encoding to be usable by machine learning models.
2. **Different Scales**: Numerical features like `Salary` and `Years of Experience` were on different scales, meaning some features could dominate others in the model unless standardized.
3. **Imbalanced Data**: The distribution of both `Work-Life Balance` and `Job Satisfaction` was skewed, which could introduce bias if not handled properly.

## Step-by-Step Process

### 1. Data Preprocessing

The first crucial step was cleaning and preparing the data. I needed to make sure the dataset was ready for analysis:
- **Encoding Categorical Variables**: I applied `OneHotEncoding` to convert categorical features into a format that the model could understand.
- **Scaling Numerical Features**: To ensure that the models treated `Salary` and `Years of Experience` equally, I standardized them to the same scale.
- **Addressing Data Imbalance**: I ensured that the training and test splits reflected the real-world distribution of the data, as an imbalanced dataset could lead to misleading results.

### 2. Feature Engineering

Next, I focused on creating features that could provide deeper insights:
- **Interaction Features**: I combined features like `Salary` and `Work-Life Balance` to capture more complex relationships.
- **Feature Selection**: Using `Random Forest Feature Importance`, I ranked and selected the most relevant features for the prediction task, ensuring that only the most impactful data was used to train the model.

### 3. Model Building and Evaluation

For the model, I decided to go with a **Random Forest Regressor** because of its balance between performance and interpretability:
- **Hyperparameter Tuning**: To get the best results, I used `GridSearchCV` to fine-tune parameters like the number of trees and maximum depth.
- **Evaluation Metrics**:
  - **R² Score**: 0.87, indicating the model could explain 87% of the variance in job satisfaction.
  - **MSE**: 0.0126, showing low error.
  - **MAE**: 0.067, reflecting minimal deviation between actual and predicted values.

## Challenges & How I Overcame Them

Like any project, I encountered challenges. Here's how I dealt with them:

1. **Imbalanced Data**: The skewed distributions in job satisfaction and work-life balance could lead to biased models. To overcome this, I used careful train-test splits and employed resampling techniques.
2. **Feature Explosion**: With so many features, it was easy to end up with redundant or less useful data. I used feature selection to cut down the noise and focus on the most important variables.
3. **Model Interpretability**: Random Forests are great for performance, but they can be hard to interpret. To make the results more understandable, I focused on explaining the feature importance and the key drivers of job satisfaction.

## Key Insights

### 1️⃣ What Drives Job Satisfaction?

The analysis revealed several key factors that drive job satisfaction:
- **Salary (0.68)**: Unsurprisingly, money matters. Employees with higher salaries tended to report higher satisfaction levels.
- **Years of Experience (0.67)**: More experienced workers appeared to have greater job satisfaction, possibly due to their alignment with career expectations and goals.
- **Work-Life Balance (0.64)**: A healthy balance between work and personal life was also a strong contributor to job satisfaction.

💡 **Surprising Insight**: Contrary to popular belief, factors like **education level** and **field of study** had little to no impact on job satisfaction. This was an eye-opening finding that challenges the conventional wisdom often shared in the HR community.

---

### 2️⃣ Predicting Satisfaction with Machine Learning

The model performed impressively well:
- **R² Score: 0.87**: Our predictions were very close to the actual satisfaction levels, proving the power of machine learning.
- **Low Errors**: Both MSE and MAE values were low, which meant the model was highly reliable.

📊 **Visualization Wins**: A scatter plot of actual vs. predicted satisfaction revealed a close match, while a prediction error heatmap highlighted areas where the model could improve.

---

### 3️⃣ The Random Forest Edge

When I compared different algorithms, **Random Forest Regressor** was the clear winner:
- **Best Performance**: It consistently delivered the lowest error rates compared to other models like linear regression and gradient boosting.
- **Robust Results**: The high R² scores across all tested models validated the effectiveness of the feature engineering and data preparation.

## Final Thoughts

This project was an incredible learning experience. It gave me a deeper appreciation for the entire data science pipeline, from understanding the data to building and tuning a model. It also taught me:
- The importance of starting with clean, well-understood data.
- How small mistakes can lead to significant learning opportunities.
- The value of storytelling in data science—taking raw numbers and turning them into actionable insights.

## What’s Next?

Looking ahead, there’s plenty more to explore:
- I plan to deploy the model to provide real-time predictions of employee satisfaction.
- Expanding the dashboard to include interactive filters for a more dynamic experience.
- Applying the same techniques to other HR datasets to explore broader trends and improve predictive models.

## Let’s Connect!

I’d love to hear your thoughts or discuss similar projects. Feel free to reach out and connect!

Check out the full project on [GitHub](Insert GitHub Link) for the code, visualizations, and more insights.
