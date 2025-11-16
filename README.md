# 🍷 Wine Sales Forecasting — Time Series Analysis (Rose & Sparkling)

This project analyzes and forecasts monthly sales of Rose Wine and Sparkling Wine from 1980–1995 using classical time series forecasting techniques. The goal is to understand seasonal patterns, evaluate predictive models, and generate 12-month future forecasts to support business decisions for ABC Estate Wines.

---

## 📂 Project Overview

Two datasets are analyzed independently:

- **Rose Wine Sales (1980–1995)**
- **Sparkling Wine Sales (1980–1995)**

Each dataset undergoes the full forecasting workflow, including:
- EDA & trend–seasonality analysis  
- Decomposition (additive & multiplicative)  
- Train-test split (train: 1980–1990 / test: 1991–1995)  
- Model building & evaluation using RMSE  
- ARIMA/SARIMA modeling (manual + automated)  
- Final model selection & 12-month future forecast  

---

## 🧪 Techniques & Models Applied

### **1. Exploratory Data Analysis (EDA)**
- Yearly & monthly boxplots  
- Empirical distribution  
- Seasonal patterns  
- Month-wise sales comparisons  
- Missing value treatment (Rose only)

### **2. Smoothing Models**
- Simple Average  
- Naïve Forecast  
- Moving Average (various windows)  
- Simple Exponential Smoothing (SES)  
- Double Exponential Smoothing (Holt)  
- Triple Exponential Smoothing (Holt-Winters)

### **3. Stationarity Testing**
- Augmented Dickey-Fuller (ADF) test  
- First differencing  
- Seasonal differencing where needed  

### **4. ARIMA/SARIMA**
- Auto ARIMA based on AIC  
- Seasonal ARIMA with period 12 and 24  
- Manual ARIMA/SARIMA using ACF/PACF cut-offs  

---

## 🏆 Best Model Findings

### **Rose Wine**
- **Best model:** 2-point Trailing Moving Average  
- **RMSE:** 11.53  
- Strong year-end seasonality (Oct–Dec)  
- Sales drop over the years; lowest in April  

### **Sparkling Wine**
- **Best model:** Triple Exponential Smoothing  
  - α = 0.03, β = 0.02, γ = 0.06  
- **RMSE:** 370.58  
- Stable sales across years except 1995  
- Peak in Oct–Dec; lowest in February  

---

## 📈 Forecasting Output
- 12-month ahead predictions generated using the best model for each wine category  
- Confidence intervals (95%) included  
- Forecasts show strong year-end demand surges  

---

## 🧠 Business Insights & Recommendations

### Common across both wines:
- Promote sales in low-demand months (Feb/Apr)
