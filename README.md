Medical Cost Prediction using Regression Analysis

An end-to-end machine learning project that predicts medical insurance costs through an iterative modeling approach, culminating in a high-accuracy Polynomial Regression model deployed via a web application.

Project Overview

This project aims to predict individual medical costs billed by health insurance based on a set of personal attributes. The analysis follows a deliberate, iterative workflow, beginning with a simple baseline model and progressively incorporating more complex techniques to enhance predictive accuracy. The primary goal is to identify the key factors that drive insurance charges and to deploy the final, most robust model into a practical, user-facing application.

Key Features

Iterative Modeling: Demonstrates a systematic approach by building and evaluating Simple, Multiple, and Polynomial Regression models.

Feature Engineering: Utilizes One-Hot Encoding for categorical data and engineers Polynomial Features to capture non-linear relationships.

Model Diagnostics: Employs visual analysis of model performance (e.g., "Actual vs. Predicted" plots) to identify limitations and guide model improvements.

Deployment: The final model is serialized using pickle and deployed via a Flask backend, showcasing an end-to-end project lifecycle.

Modeling Workflow & Findings

The project progressed through three key modeling stages, each revealing deeper insights.

Stage 1: Baseline Model (Simple Linear Regression)

A baseline was established using a single feature, Body Mass Index (bmi), to predict charges.

Result: The model yielded a very low R-squared of ~4%.

Conclusion: This confirmed that bmi alone is insufficient for making accurate predictions, necessitating a more comprehensive feature set.

Stage 2: Enhanced Model (Multiple Linear Regression)

The model was improved by including all relevant features: age, bmi, children, sex, smoker, and region.

Result: Performance improved dramatically to an R-squared of ~78%.

Key Insight: Coefficient analysis revealed that being a smoker was the single most significant factor, increasing predicted costs by over $23,000.

Limitation: Diagnostics revealed that predictions became less accurate for higher-cost individuals, suggesting uncaptured non-linear patterns.

Stage 3: Advanced Model (Polynomial Regression)

To address the limitations of the linear model, Polynomial Features (degree 2) were engineered. This technique creates interaction and squared terms (e.g., age^2, age * bmi) to fit more complex, non-linear relationships.

Result: This model achieved the highest performance, with an R-squared of ~85%.

Conclusion: The significant accuracy increase confirms that medical costs have a non-linear relationship with patient attributes, which the Polynomial Regression model successfully captured.

Model Performance Summary

Model

R-squared Score

Key Takeaway

Simple Linear Regression

~4%

A single feature is not enough.

Multiple Linear Regression

~78%

Multiple features provide good predictive power.

Polynomial Regression

~85%

Capturing non-linearity is key to high accuracy.

This iterative process demonstrates a complete analytical workflow: starting simple, identifying model weaknesses through diagnostics, and applying advanced techniques to build a robust and highly accurate predictive model ready for deployment.
