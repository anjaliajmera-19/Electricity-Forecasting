# Electricity-Forecasting
Electricity Forecasting Using Machine Learning and Deep Learning

**Objective**

The objective of this project is to develop time-series forecasting models for predicting electricity prices using historical energy generation, electricity load, and weather data.

The project integrates energy and weather datasets to create a multivariate time-series forecasting problem. It explores the relationship between electricity parameters and weather conditions and applies Machine Learning and Deep Learning techniques to improve forecasting accuracy.

**About the Dataset**

The project uses two datasets:

1. Energy Dataset (energy_dataset.csv)

Contains historical electricity data, including:

Electricity generation from different sources such as solar, wind, nuclear, hydro, and fossil fuels.

Actual and forecasted electricity load.

Day-ahead and actual electricity prices.

Timestamp information.

2. Weather Dataset (weather_features.csv)

Contains weather information from five Spanish cities:

Valencia

Madrid

Bilbao

Barcelona

Seville

Weather parameters include temperature, humidity, atmospheric pressure, wind speed, wind direction, rainfall, snowfall, and cloud coverage.

Both datasets are integrated using timestamps to incorporate weather conditions into electricity forecasting.

**Method**

The project consists of the following main steps:

Data Loading and Exploration: Loading energy and weather datasets, examining data distributions, and analyzing feature correlations.

Data Preprocessing: Handling missing values, removing duplicates, identifying outliers, and integrating both datasets.

Feature Engineering: Extracting hour, weekday, month, and year from timestamps and combining selected energy generation features.

Time-Series Analysis: Applying Seasonal Decomposition, Augmented Dickey-Fuller (ADF) Test, ACF, and PACF to study trends, seasonality, and stationarity.

Dimensionality Reduction: Applying MinMax Scaling and Principal Component Analysis (PCA) while retaining 80% cumulative variance.

Model Building and Training: Developing forecasting models using XGBoost and GRU with a historical window of 24 observations.

Model Evaluation: Comparing actual and predicted electricity prices using Mean Absolute Error (MAE).

**Requirements**

To run the project, install the following libraries:

NumPy

Pandas

Matplotlib

Seaborn

Plotly

Scikit-learn

XGBoost

TensorFlow / Keras

Statsmodels

Install using:

pip install numpy pandas matplotlib seaborn plotly scikit-learn xgboost tensorflow statsmodels

**Motivation**

Electricity demand and pricing are influenced by several factors, including energy generation patterns, consumption trends, and weather conditions.

This project aims to explore these relationships and develop forecasting models that can:

Analyze the impact of weather conditions on electricity generation and pricing.

Identify temporal patterns in electricity prices.

Compare actual electricity prices with day-ahead price predictions.

Improve electricity price forecasting using Machine Learning and Deep Learning approaches.

**Models Used**

1. Machine Learning

XGBoost Regressor

2. Deep Learning

GRU (Gated Recurrent Unit)

**Results**

The models were evaluated using Mean Absolute Error (MAE) on the normalized test dataset.

Model-Test MAE

XGBoost-0.016

GRU-0.018
