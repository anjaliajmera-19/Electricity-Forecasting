# Electricity-Forecasting
Electricity Forecasting Using Machine Learning and Deep Learning

**Project Overview**

This project focuses on electricity forecasting using historical energy generation, electricity load, electricity pricing, and weather data.

The objective is to analyze historical electricity trends and develop predictive models capable of forecasting electricity prices by considering temporal patterns, energy generation characteristics, and weather conditions.

The project combines data preprocessing, exploratory data analysis (EDA), feature engineering, dimensionality reduction, and time-series forecasting using Machine Learning and Deep Learning techniques.

**Objectives**

Analyze historical electricity generation, load, and price patterns.

Explore the relationship between electricity parameters and weather conditions.

Perform data cleaning and preprocessing to handle missing values, duplicates, and outliers.

Identify important features through correlation analysis.

Apply Principal Component Analysis (PCA) for dimensionality reduction.

Analyze time-series characteristics such as trend, seasonality, and stationarity.

Develop and evaluate forecasting models using XGBoost and GRU.

**Dataset Description**

The project uses two datasets:

1. Energy Dataset (energy_dataset.csv)

Contains historical electricity-related information, including:

Electricity generation from different sources (solar, wind, nuclear, hydro, fossil fuels, etc.).

Actual and forecasted electricity load.

Day-ahead electricity prices.

Actual electricity prices.

Timestamp information.

2. Weather Dataset (weather_features.csv)

Contains weather observations from five Spanish cities:

Valencia

Madrid

Bilbao

Barcelona

Seville

Weather parameters include:

Temperature

Atmospheric pressure

Humidity

Wind speed and direction

Rainfall

Snowfall

Cloud coverage

The two datasets are integrated using their corresponding timestamps to incorporate weather conditions into electricity forecasting.

**Methodology**

1. Data Preprocessing
2.Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Time-Series Analysis
5. Dimensionality Reduction
6. Model Development:
Two forecasting models were implemented:

**XGBoost Regressor**

Used historical time-windowed observations as input.

Reshaped sequential data into a two-dimensional format.

Trained using training and validation datasets.

Used Mean Absolute Error (MAE) as the evaluation metric.

Implemented early stopping.

**GRU (Gated Recurrent Unit)**

Developed a sequential deep learning architecture.

Used a GRU layer with 32 units.

Applied Flatten and Dense layers.

Incorporated Dropout (0.1) to reduce overfitting.

Used Adam optimizer with Cosine Decay Restarts learning rate scheduling.

Applied Early Stopping during training.

**Model Performance**

The dataset was divided chronologically into:

Training: 80%

Validation: 10%

Testing: 10%

A historical window of 24 observations was used for forecasting.

Model

Test MAE (Normalized)

XGBoost-0.016

GRU-0.018

The results indicate that XGBoost achieved a slightly lower test MAE than the GRU model in the implemented experiment.

Note: The reported MAE values are calculated on normalized target values, not the original electricity price scale.

**Technologies and Libraries Used**

Programming Language: Python

Libraries:

NumPy

Pandas

Matplotlib

Seaborn

Plotly

Scikit-learn

XGBoost

TensorFlow / Keras

Statsmodels
