# Covid-19-Case-Prediction
Project Overview: 

This project aims to forecast future COVID-19 confirmed cases and death counts using historical data by applying regression techniques, specifically linear and polynomial regression. The dataset consists of multiple CSV files containing global and US COVID-19 data in both "CONVENIENT" and "RAW" formats.

We use time-series data, aggregate it by country/region, and predict the trend of cases/deaths for the next 30 days.

Files and Dataset
The project reads the following CSV files from a Google Drive folder:

CONVENIENT_global_confirmed_cases.csv

CONVENIENT_global_deaths.csv

CONVENIENT_us_confirmed_cases.csv

CONVENIENT_us_deaths.csv

RAW_global_confirmed_cases.csv

RAW_global_deaths.csv

RAW_us_confirmed_cases.csv

RAW_us_deaths.csv

Plus associated metadata files which are not used for forecasting.

How to Run
Mount Google Drive in your Colab environment.

Set the path to the folder containing the datasets.

Run the provided Python script to load data, preprocess it, perform regression, and visualize forecasts.

Key Steps in Code
Mount Google Drive: Access files stored in Drive.

Load CSV files: Read all CSV files into a dictionary for easy access.

Preprocessing: Drop unnecessary columns like latitude and longitude, group data by country/region, and transpose so dates become rows.

Feature Engineering: Calculate "Days Since" the first recorded date to use as a numeric feature.

Regression: Split data into train/test sets, fit linear and polynomial regression models.

Evaluation: Calculate mean squared error (MSE) and R² score for performance.

Forecasting: Predict confirmed cases/deaths for next 30 days.

Visualization: Plot actual data, model predictions, and forecasts.

Dependencies
Python 3.x

pandas

numpy

matplotlib

scikit-learn

Google Colab (recommended)
