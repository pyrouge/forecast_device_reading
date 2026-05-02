## Forecasting & Anomaly Detection Pipeline
## Overview
This script builds a complete pipeline for time-series forecasting and anomaly detection using sensor readings. It processes raw data, detects anomalies, trains machine learning models, evaluates performance, and generates future forecasts.

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/0c482a77-7f00-4833-a10b-92d1f63173b7" />

## Features
Data Cleaning: Handles missing values, duplicates, and resamples to 5-second intervals.

Anomaly Detection: Uses the IQR method to flag outliers.

Quartile Analysis: Provides descriptive statistics of readings.

## Forecasting Model:

Predicts readings 3 hours ahead using HistGradientBoostingRegressor (optionally ensembles with LightGBM).

Includes lag features, rolling statistics, and cyclical time features.

Applies bias correction and multiplicative calibration.

## Evaluation Metrics: 
Computes MAE, RMSE, MAPE, SMAPE, bias, and classification accuracy (directional up/down/flat).

## Future Forecast Generation: 
Produces predictions for the next 3 hours and saves them to CSV.

## Requirements
Python 3.8+

Libraries: pandas, numpy, matplotlib, scikit-learn, seaborn (optional), lightgbm (optional), openpyxl

Install dependencies:
_pip install pandas numpy matplotlib scikit-learn seaborn lightgbm openpyxl_

**Usage**
Place your dataset (.xlsx) in the project folder.
Update the file_path variable in the script.

Run the script: python main.py
## Outputs:

evaluation_metrics.json → Model performance metrics

future_predictions_generated.csv → Forecasted readings
