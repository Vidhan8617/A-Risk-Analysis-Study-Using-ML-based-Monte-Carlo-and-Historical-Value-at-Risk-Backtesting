# A-Risk-Analysis-Study-Using-ML-based-Monte-Carlo-and-Historical-Value-at-Risk-Backtesting
This project compares Historical VaR and ML-based Monte Carlo VaR for market risk analysis on Indian stock data. Volatility is predicted using a Random Forest model and used in Monte Carlo simulations. Both models are backtested using violation rates and binomial tests.

🧑‍💻 Tools & Libraries

Python, Pandas, NumPy

Scikit-learn

SciPy

Matplotlib

🔧 Techniques Used

Historical Value at Risk (99%)

Random Forest regression for volatility prediction

Monte Carlo simulation for loss distribution modeling

Student-t distribution for fat-tailed returns

Out-of-sample backtesting

Exact binomial test for VaR validation

Methodology

The objective of this project is to evaluate and compare traditional and machine-learning-enhanced Value at Risk (VaR) models using Indian stock market data. The methodology follows a structured pipeline consisting of data preprocessing, risk modeling, simulation, and statistical backtesting.

Data Preparation

Daily price data from the Indian equity market was collected and preprocessed by parsing dates, sorting observations chronologically, and converting price values into numerical format. Daily log returns were computed from adjusted closing prices and used as the basis for all risk calculations.

Train–Test Split

To avoid look-ahead bias, the dataset was split chronologically into training and testing sets. All model estimation was performed using the training data, while risk forecasts were evaluated exclusively on out-of-sample test data.

Historical VaR

As a traditional baseline, 99% Historical VaR was estimated by computing the 1st percentile of the training-period return distribution. This resulted in a fixed risk threshold, which was subsequently backtested against test-period losses.

ML-Based Volatility Modeling

For the Monte Carlo VaR framework, rolling volatility was modeled using a Random Forest regression algorithm. Input features included lagged returns, rolling averages, and volatility persistence terms. The trained model generated daily volatility forecasts for the test period.

Monte Carlo Simulation

Using the predicted volatility estimates, Monte Carlo simulations were performed to generate thousands of potential future returns for each day. To better capture fat-tailed behavior in financial returns, a Student-t distribution was employed. The 99% VaR was obtained as the lower-tail quantile of the simulated loss distribution.

Backtesting and Validation

Both Historical VaR and ML-based Monte Carlo VaR were backtested by comparing predicted VaR thresholds against realized out-of-sample losses. Violation rates were computed and evaluated using the exact binomial test to assess statistical consistency with the assumed confidence level.

Model Comparison

The two approaches were compared based on violation frequency, statistical validation results, and visual inspection. This enabled an assessment of static versus adaptive risk modeling and highlighted the benefits of machine-learning-enhanced Monte Carlo VaR.



🧠 Methodology Summary

Preprocess Indian stock market price data

Compute daily returns and rolling volatility

Split data into training and testing sets (time-series aware)

Estimate Historical VaR from training data

Train an ML model to predict volatility

Generate Monte Carlo simulations using predicted volatility

Estimate 99% Monte Carlo VaR

Backtest both models on test data

Validate results using violation rates and binomial tests

Compare static and adaptive risk models
<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/b9f37f61-fb25-46fa-bd47-ba72967d01c6" />
