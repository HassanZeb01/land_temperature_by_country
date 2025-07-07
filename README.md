#  Global Land Temperature and CO2 Emission
## Time Series Forecasting and Regression Analysis

## 📌 Project Overview
Forecasting land temperature and analyzing the relationship between CO₂ emissions and temperature using SARIMA, LSTM, and Random Forest models.

## 🧠 Objectives
- Forecast land temperature using time series models
- Analyze the relationship between logged CO₂ emissions and temperature
- Compare model performance using MSE and RMSE

## 📊 Dataset
- **Climate Change: Earth Surface Temperature Data:** [https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data/data]
- **CO₂ Emissions:** [[Source name](https://www.kaggle.com/datasets/ulrikthygepedersen/co2-emissions-by-country)]
- Format: CSV files / SQLite / JSON (mention whatever applies)

## 🛠️ Models Used
- **SARIMA** for seasonal trend forecasting
- **LSTM** for deep learning-based forecasting
- **Random Forest** for regression analysis between CO₂ and temperature

## 📈 Results
| Model        | MSE     | RMSE   |
|--------------|---------|--------|
| SARIMA       | 0.0999  | 0.3160 |
| LSTM         | 0.1095  | 0.3309 |
| Random Forest| 32.0152 | 5.6582 |

- SARIMA performed best for forecasting.
- Random Forest showed weak correlation, suggesting CO₂ alone doesn't explain temperature changes.
