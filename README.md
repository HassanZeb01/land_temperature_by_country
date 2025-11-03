# 🌍 Global Land Temperature Forecasting and CO₂ Emission Analysis

## 📖 Overview
This project aims to forecast **global land temperature** and analyse its relationship with **CO₂ emissions** using time series and machine learning techniques.  
Two datasets were obtained from **Kaggle** — *Global Land Temperature* and *CO₂ Emission* — to study long-term temperature trends and their potential connection to greenhouse gases.

The study is divided into:
1. **Phase 1:** Temperature forecasting using SARIMA and LSTM.
2. **Phase 2:** Regression analysis using Random Forest to measure the relationship between temperature and CO₂ emissions.

---

## 🎯 Objectives
- Forecast global land temperature using statistical and deep learning models.  
- Compare the performance of SARIMA and LSTM models.  
- Analyse the correlation between CO₂ emissions and temperature using Random Forest regression.  
- Identify strengths and limitations of different predictive methods.

---

## 🧠 Methodology

### Phase 1: Temperature Forecasting
**Dataset:** Global Land Temperature (1743–2013) from Berkeley Earth via Kaggle  
**Models Used:**  
- SARIMA (Seasonal ARIMA): Captures linear and seasonal patterns.  
- LSTM: Models nonlinear and long-term dependencies.

**Evaluation Metrics:**  
Mean Squared Error (MSE) and Root Mean Squared Error (RMSE)  

| Model | MSE | RMSE |
|--------|------|------|
| SARIMA | 0.0999 | 0.3160 |
| LSTM | 0.1089 | 0.3299 |

SARIMA slightly outperformed LSTM, showing stronger ability to model seasonal temperature trends.

---

### Phase 2: CO₂–Temperature Relationship
**Dataset:** CO₂ Emissions (1960–2019) from UNFCCC and IEA  
**Model:** Random Forest Regression  

| Metric | Value |
|---------|--------|
| MSE | 31.3190 |
| RMSE | 5.5963 |

**Interpretation:**  
CO₂ emissions show a quantifiable but weak relationship with global land temperature.  
This may be due to data granularity differences (annual CO₂ vs monthly temperature) and missing factors like methane, aerosols, and oceanic heat retention.

---

## ⚙️ Tools & Libraries
- **Python**
- Pandas, NumPy
- Matplotlib, Seaborn
- Statsmodels
- TensorFlow / Keras
- Scikit-learn

---

## 📊 Key Findings
- SARIMA captured seasonal trends better than LSTM.  
- LSTM performed reasonably well but required more tuning.  
- Random Forest showed CO₂ has a measurable yet weak influence on temperature.  

---

## 🚀 Future Work
- Include additional climate factors (methane, humidity, ocean temperature).  
- Use advanced deep learning models (BiLSTM, GRU, CNN-LSTM).  
- Apply hyperparameter tuning and cross-validation.  
- Extend analysis to regional forecasting.

---


---

## 🧩 Conclusion
The project shows how traditional models like **SARIMA** can outperform **LSTM** for seasonal datasets.  
While CO₂ emissions influence temperature, they are not the sole factor driving global warming.  
This research demonstrates the value of applying machine learning to climate data forecasting.

---

## 👤 Author
**Hassan Zeb**  
📍 London, United Kingdom
