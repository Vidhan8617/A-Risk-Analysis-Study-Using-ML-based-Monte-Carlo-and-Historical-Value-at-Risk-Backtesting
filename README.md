# 📉 A Risk Analysis Study Using ML-Based Monte Carlo and Historical Value at Risk (VaR)

This project presents a comparative market risk analysis using **Historical Value at Risk (VaR)** and an **ML-based Monte Carlo VaR** framework applied to **Indian stock market data**.  
Volatility is predicted using a **Random Forest regression model** and incorporated into Monte Carlo simulations.  
Both approaches are evaluated using **out-of-sample backtesting** and **statistical validation**.

---

## 🚀 Project Highlights

- Comparison of static and adaptive VaR models  
- Machine Learning–based volatility forecasting  
- Monte Carlo simulations with fat-tailed distributions  
- Robust statistical backtesting using binomial tests  
- Application on real Indian equity market data  

---

## 🧑‍💻 Tools & Libraries

- Python  
- Pandas, NumPy  
- Scikit-learn  
- SciPy  
- Matplotlib  

---

## 🔧 Techniques Used

- Historical Value at Risk (99% confidence level)  
- Random Forest regression for volatility prediction  
- Monte Carlo simulation for loss distribution modeling  
- Student-t distribution for fat-tailed returns  
- Time-series aware train–test split  
- Out-of-sample backtesting  
- Exact binomial test for VaR validation  

---

## 📌 Methodology

The objective of this project is to evaluate and compare traditional and machine-learning-enhanced Value at Risk (VaR) models using Indian stock market data. The methodology follows a structured and bias-free pipeline.

---

### 1. Data Preparation

- Collected daily price data from the Indian equity market  
- Parsed dates and sorted observations chronologically  
- Converted price values into numerical format  
- Computed daily log returns from adjusted closing prices  

---

### 2. Train–Test Split

- Dataset split chronologically to avoid look-ahead bias  
- Model estimation performed only on training data  
- Risk forecasts evaluated exclusively on out-of-sample test data  

---

### 3. Historical VaR

- Estimated 99% Historical VaR as a baseline model  
- Computed the 1st percentile of training-period returns  
- Generated a fixed risk threshold  
- Backtested against test-period losses  

---

### 4. ML-Based Volatility Modeling

- Modeled rolling volatility using Random Forest regression  
- Input features included:
  - Lagged returns  
  - Rolling averages  
  - Volatility persistence terms  
- Generated daily volatility forecasts for the test period  

---

### 5. Monte Carlo Simulation

- Used predicted volatility estimates to simulate thousands of future returns per day  
- Applied a Student-t distribution to capture fat-tailed behavior  
- Estimated 99% Monte Carlo VaR from the lower-tail quantile of simulated losses  

---

### 6. Backtesting and Validation

- Compared predicted VaR thresholds against realized losses  
- Computed violation rates for both models  
- Applied the exact binomial test to assess statistical consistency  

---

### 7. Model Comparison

- Compared Historical VaR and ML-based Monte Carlo VaR using:
  - Violation frequency  
  - Statistical test results  
  - Visual performance analysis  
- Highlighted the advantages of adaptive ML-based risk modeling over static approaches  

---

## 🧠 Methodology Summary

- Preprocess Indian stock market price data  
- Compute daily returns and rolling volatility  
- Perform time-series aware train–test split  
- Estimate 99% Historical VaR  
- Train an ML model to predict volatility  
- Generate Monte Carlo simulations using predicted volatility  
- Estimate 99% Monte Carlo VaR  
- Backtest both models on test data  
- Validate results using violation rates and binomial tests  
- Compare static and adaptive risk models  

---

## 📈 Conclusion

This study demonstrates that **machine-learning-enhanced Monte Carlo VaR** provides a more adaptive and responsive framework for market risk estimation compared to traditional Historical VaR, particularly under changing market volatility conditions.


