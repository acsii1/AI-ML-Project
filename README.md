AI/ML Project

⸻

1️⃣ Introduction

This project focuses on building a model to predict the number of bikes rented at any given hour in Seoul based on historical data, weather conditions, and time features.

The practical problem addressed: Some bike stations run out of bikes quickly during rush hours, while others remain unused. This causes inefficiency in bike distribution and lower user satisfaction.

The goal of this project is to provide a data-driven AI/ML solution that helps bike-sharing companies optimize bike distribution and improve service efficiency.

⸻

2️⃣ Dataset Overview

We used the Seoul Bike Sharing Demand Dataset, which contains hourly data for an entire year (8760 hours).

The dataset includes:
 • Time features: hour, day, month, weekday
 • Weather features: temperature, humidity, wind speed, visibility, solar radiation, rainfall, snowfall
 • Additional features: season, holiday or working day, functioning day

Target variable: Number of rented bikes per hour.

⸻

3️⃣ Data Processing & Feature Engineering

Before building the models, several preprocessing steps were performed:
 1. Data Cleaning: Column names were simplified for clarity and ease of use.
 2. Feature Extraction: The date column was split into day, month, and weekday to create new features.
 3. Categorical Encoding: Variables like season, holiday, and functioning day were converted into numerical formats suitable for machine learning.
 4. New Feature Creation: Added Day_Type to indicate whether it’s a workday or leisure day.

These steps resulted in a clean dataset ready for model training with 21 columns.

⸻

4️⃣ Exploratory Data Analysis (EDA)

Data analysis was performed to understand patterns and relationships:
 • Hourly Demand: Peak hours were identified where bike rentals spike significantly.
 • Weather Impact: Temperature, humidity, and rainfall were found to directly influence the number of bikes rented.
 • Seasonal Trends: Summer showed higher demand compared to winter.
 • Feature Relationships: Correlations between variables were studied to identify the most influential factors.

⸻

5️⃣ Machine Learning Modeling

Two predictive models were built:
 1. Linear Regression:
 • A simple linear model assuming a direct relationship between features and bike rentals.
 • Provided decent predictions but could not capture complex non-linear relationships.
 2. Random Forest Regressor:
 • A tree-based model capable of capturing non-linear relationships.
 • Delivered much higher accuracy and lower error compared to Linear Regression.

Performance Metrics:
 • Linear Regression: R² ≈ 0.54, RMSE ≈ 435
 • Random Forest: R² ≈ 0.93, RMSE ≈ 169

Conclusion: Random Forest performed better due to its ability to handle complex, non-linear interactions between time, weather, and bike rental demand.

⸻

6️⃣ Real-World Test Scenario

A real-world prediction was performed using the models:
 • Scenario: Monday, Summer, 8:00 AM, 25°C, no rain, workday.
 • Predictions:
 • Linear Regression: ~907 bikes
 • Random Forest: ~1968 bikes

Analysis: The Random Forest prediction is more realistic because it captures the non-linear effects of weather and time variables, whereas Linear Regression underestimates the demand.

⸻

7️⃣ Skills & Learnings

From this project, the following AI/ML skills were acquired:
 • Data preprocessing and feature engineering
 • Exploratory data analysis (EDA) and visualization
 • Building and evaluating machine learning models (Linear Regression & Random Forest)
 • Model evaluation using R² and RMSE
 • Understanding feature importance and non-linear relationships
 • Applying models to real-world scenarios for practical predictions

⸻

8️⃣ Conclusion

This project demonstrates the practical application of AI/ML to solve real-world problems.
Random Forest provided the most accurate predictions, showing its strength in capturing complex patterns in data.
The project highlights how predictive modeling can help optimize bike-sharing operations, improve resource allocation, and increase user satisfaction.
