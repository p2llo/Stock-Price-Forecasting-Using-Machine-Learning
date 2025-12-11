# 📈 Stock Price Forecasting Using Machine Learning 

This project builds an **end-to-end machine learning pipeline** to forecast **Apple (AAPL)** stock closing prices using historical financial data.
It includes **EDA**, **feature engineering**, and **ML models** such as **Random Forest Regressor** and **XGBoost Regressor**, with comparison against a baseline.

Dataset Source: Kaggle – *Stocks Historical Price Data*

---

## 🔍 Project Overview

This project demonstrates a complete stock forecasting workflow:

1. Load multi-stock price dataset
2. Select a single stock (AAPL)
3. Perform Exploratory Data Analysis (EDA)
4. Engineer powerful time-series features
5. Train ML models (RF, XGBoost)
6. Evaluate performance using RMSE & MAE
7. Visualize predictions vs actual values

---

## 🗂 Dataset Description

Each stock file contains:

* **Date**
* **Open**
* **High**
* **Low**
* **Close**
* **Adj Close** (if available)
* **Volume**
* **Ticker**

Data is historical OHLC format and sourced directly from Yahoo Finance.

Folder path in Kaggle Notebook:

```
/kaggle/input/stocks-historical-price-data/historical_data
```

---

## 📊 Exploratory Data Analysis (EDA)

EDA includes:

### Stock Closing Price Trend

* Line plot of closing prices over time

### Volume Trend

* Trading volume distribution
* Volume fluctuations across time

### Statistical Analysis

* Summary statistics
* Missing value inspection

---

## 🧠 Feature Engineering

Created predictive features include:

### Lag Features

* `Close_lag_1`, `Close_lag_5`, `Close_lag_10`

### Returns

* Daily percent returns

### Technical Indicators

* **SMA (10-day Simple Moving Average)**
* **EMA (10-day Exponential Moving Average)**
* **MACD (12/26 EMA difference)**
* **RSI (14-day Relative Strength Index)**

These features significantly improve model performance for short-term forecasting.

---

## 🤖 Models Used

### **1. Random Forest Regressor**

* Captures non-linear price dynamics
* Performs well with engineered features

### **2. XGBoost Regressor**

* Gradient boosting model
* Highly effective on structured tabular data
* Typically outperforms Random Forest on this task

### **3. Baseline**

* Naive lag-based prediction for comparison

---

## 📈 Evaluation Metrics

Models were evaluated using:

* **RMSE** (Root Mean Squared Error)
* **MAE** (Mean Absolute Error)

These metrics were computed on the final 20% test set.

---

## 📉 Forecast Visualization

The final output includes a line plot comparing:

* Actual Closing Prices
* Random Forest Predictions
* XGBoost Predictions

This visual clearly shows how well each model tracks real market movements.

---

## 🧪 Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* Scikit-learn
* XGBoost
* Jupyter Notebook / Kaggle Notebook

---

## 📬 Results Summary

* XGBoost outperforms Random Forest in most runs
* Technical indicators (SMA, EMA, MACD, RSI) significantly improve forecasting accuracy
* Lag features help capture daily momentum
* Final prediction curves closely follow actual prices

---

## 🧾 Future Improvements

* Add ARIMA/SARIMAX baseline for comparison
* Hyperparameter tuning with Optuna
* Try LightGBM or CatBoost
* Multi-stock forecasting
* Build a Streamlit UI dashboard

---

## ⭐ Acknowledgements

Dataset: *Stocks Historical Price Data* (Kaggle)
