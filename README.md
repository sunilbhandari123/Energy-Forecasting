# Electricity_Demand_and_Price_forecasting


# Objective: 

This project focuses on multivariate time series forecasting by integrating energy consumption and weather data from multiple cities in Spain. By combining electricity demand, generation, pricing, and weather-related variables, the project addresses the challenge of forecasting time-dependent electricity demand and prices in a complex, real-world setting.

A range of advanced forecasting models were implemented, including XGBoost Regressor, GRU, LSTM, CNN, CNN–LSTM, and LSTM with Attention. In addition, hybrid ensemble approaches such as GRU–XGBoost and LSTM-Attention–XGBoost were developed to leverage the strengths of both deep learning and tree-based models.

The goal is to generate accurate and robust forecasts that support improved decision-making in the energy sector. 
 

## About the Dataset:

The dataset combines four years of hourly electricity and weather data from Spain, forming a multivariate time series problem.
Energy data includes electricity consumption, pricing, and generation from multiple sources such as fossil fuels, wind, and coal.
Weather data includes temperature, humidity, pressure, wind speed, and related meteorological variables across different cities.

Data sources:

Electricity consumption and generation: ENTSO-E public portal
Electricity settlement prices: Red Eléctrica de España (Spanish TSO)
Weather data: OpenWeatherMap API
This integration enables detailed analysis of how weather and generation patterns influence electricity demand and pricing.

## Methodology 
The project implementation is structured into four main stages:

1. # Data Loading and Exploration

Loaded and processed datasets using Pandas
Performed exploratory analysis and correlation studies
Visualized relationships across energy and weather variables

2. # Preprocessing
Handled missing values
Extracted time-based features (hour, weekday, month, year)
Normalized and reshaped data for modeling
Applied the Augmented Dickey–Fuller test to assess stationarity

3. # Model Development and Training

Applied PCA for feature selection
Built forecasting models using XGBoost, GRU, LSTM, CNN, CNN–LSTM, and LSTM-Attention
Implemented hybrid ensemble models (GRU–XGBoost, LSTM-Attention–XGBoost)

4. # Evaluation and Comparison

Compared models using Mean Absolute Error (MAE)
Visualized training and validation performance
Evaluated forecasting accuracy across different architectures



## Requirements

To run the code, you need to install the following libraries:

- matplotlib
- Numpy, panda, math
- Seaborn
- Xgboost
- Tensorflow
- keras
- Scikit Learn 

## Motivation:
This dataset is particularly valuable due to its hourly granularity and the availability of TSO-provided forecasts for both consumption and pricing. This enables direct comparison between industry-standard forecasts and machine learning–based approaches.

Key questions explored include:

1. How do load and marginal supply curves evolve across time?
2. Which weather variables and cities most strongly influence electricity demand, pricing, and generation?
3. Can machine learning models improve the TSO’s 24-hour ahead forecasts?
4. How accurately can time-of-day electricity prices be predicted?
5. Can reliable hour-by-hour intraday forecasts for demand and pricing be achieved?

## Models used in this project : 

#### 1. Machine learning : 
 * XGboost Regressor
#### 2. Deep learning/Stacked models :
* GRU 
* LSTM 
* CNN 
* CNN-LSTM 
* LSTM-Attention 
#### 3. Hybrid methods:   
* GRU-XGBoost 
* LSTM-Attention-XGBoost 

## Results
The MAE (Mean Absolute Error) is used to report the results for the normalized test set:
* TSO prediction : 0.070
* XGboost : 0.016
* GRU : 0.015
* LSTM : 0.018
* CNN : 0.025
* CNN-LSTM : 0.019
* LSTM-Attention : 0.015
* Hybrid GRU-XGBoost : 0.014
* Hybrid LSTM-Attention-XGBoost : 0.015
  
Note : According to the findings, the hybrid methods demonstrated better performance in terms of MAE compared to other methods. It is worth mentioning that all machine learning/deep learning methods outperformed TSO prediction.

## Inspiration(insight): Ritik Dhame 
