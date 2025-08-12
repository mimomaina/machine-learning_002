# Time Series Analysis and Forecasting of PM2.5 Levels

This repository contains a Jupyter notebook that performs a comprehensive time series analysis of air quality data, with a focus on **PM2.5 concentrations**. The workflow includes exploratory data analysis, statistical decomposition, model training, and forecasting using ARIMA and Prophet.

## Dataset

The analysis uses the **PRSA_Data_20130301-20170228** dataset, which contains hourly measurements of:
- PM2.5 and PM10 pollutant levels
- Weather variables (temperature, pressure, dew point, rainfall, wind speed)
- Temporal data (year, month, day, hour)

## Objectives

- Understand patterns, trends, and seasonality in PM2.5 levels.
- Build forecasting models to predict future air quality.
- Evaluate model performance and interpret results for real-world application.

## Workflow

### 1. Introduction
PM2.5 refers to fine particulate matter that poses serious health risks. The notebook applies time series techniques to:
- Detect trends and seasonality
- Measure autocorrelation
- Forecast future PM2.5 levels

### 2. Data Preprocessing and Feature Scaling
- **StandardScaler** applied to: Temperature (TEMP), Pressure (PRES), Dew Point (DEWP)
- **MinMaxScaler** applied to: Rainfall (RAIN), Wind Speed (WSPM), PM2.5, PM10
- Ensured all features were on a comparable scale for modeling.

### 3. Exploratory Data Analysis (EDA)
- **Distribution of Rain Values**: Most days have little to no rainfall, distribution is right-skewed.
- **Rolling Statistics**: 24-hour rolling mean and standard deviation highlight long-term trends and volatility.
- **Autocorrelation Function (ACF)**: Significant autocorrelation at multiples of 24 hours, indicating daily seasonality.

### 4. Time Series Decomposition
- **Classical Seasonal Decomposition**: Shows trend, seasonal patterns, and residual noise in PM2.5 levels.
- **Prophet Model Components**: Captures long-term trend, weekly and yearly seasonality, and holiday effects.

### 5. Modeling
#### ARIMA Model
- Order: (2, 2, 0)
- Fitted on PM2.5 series after differencing for stationarity.
- Model summary used to assess parameter significance.

#### Prophet Model
- Handles strong seasonal patterns and holiday effects.
- Trained on historical PM2.5 data and tested on a hold-out set.
- Forecast evaluation using MAE and RMSE.

### 6. Model Evaluation
- **Residual Analysis**: Random scatter around zero indicates a good fit; patterns suggest missing variables.
- **Forecast Visualization**: Actual vs. predicted values with uncertainty intervals.

### 7. Conclusion
The analysis demonstrates:
- Clear seasonal patterns in PM2.5 levels.
- ARIMA and Prophet models provide reasonable forecasts.
- Insights can inform environmental policy and public health interventions.

### 8. Future Work
- Include additional predictors such as traffic and industrial activity.
- Test advanced models like LSTM and XGBoost for comparison.
- Deploy a real-time forecasting system.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- statsmodels
- fbprophet (or prophet for newer versions)

## Usage

1. Clone the repository:
   
   git clone <repo-url>
## Install dependencies:

pip install -r requirements.txt

## Run the notebook:


jupyter notebook <notebook-name>.ipynb

## License
This project is licensed under the MIT License.
