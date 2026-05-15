# Task 2: Predict Future Stock Prices (Short-Term)

## Objective
The objective of this task is to use historical stock market data to predict the next day's closing stock price using regression-based machine learning models.

---

## Dataset Used
**Source:** Yahoo Finance API  
**Library:** `yfinance`

### Selected Stock
- **Apple Inc. (AAPL)**

### Date Range
- **Start Date:** January 1, 2022
- **End Date:** December 31, 2024

---

## Features Used

Original stock indicators:

- Open
- High
- Low
- Close
- Volume

Engineered features:

- **MA_5** → 5-day moving average
- **MA_10** → 10-day moving average
- **Daily_Return** → Daily percentage change
- **Price_Range** → High − Low

---

## Target Variable
The model predicts:

**Next Day Closing Price**

(Target was created by shifting Close prices forward by one day.)

---

## Tools and Libraries Used
- Python
- Pandas
- NumPy
- Matplotlib
- yfinance
- Scikit-learn

---

## Models Applied

### 1. Linear Regression
A baseline regression model used to capture linear relationships between stock features and next-day closing price.

---

### 2. Random Forest Regressor
An ensemble-based machine learning model capable of learning non-linear relationships and complex feature interactions.

Configuration:

- `n_estimators = 100`
- `random_state = 42`

---

## Data Preprocessing

### MultiIndex Handling
Flattened stock columns when required.

### Missing Value Handling
Rows with NaN values were removed.

### Feature Scaling
StandardScaler was applied before training.

### Train-Test Split
- **80% Training**
- **20% Testing**

Time-based splitting was used to preserve chronological order.

---

## Model Evaluation Metrics

Models were evaluated using:

- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**
- **R² Score**

These metrics assess:

- Prediction accuracy
- Error magnitude
- Goodness of fit

---

## Visualizations Created

### Stock Price History
Shows historical closing prices over time.

---

### Trading Volume Plot
Displays volume fluctuations.

---

### Actual vs Predicted Prices
Compares predicted closing prices with actual market prices.

---

### Feature Importance Plot
Shows which features contributed most to Random Forest predictions.

---

## Key Results and Findings

### Linear Regression
Performed well for capturing overall price trends.

Strength:
- Simplicity
- Interpretability

Limitation:
- Limited ability to capture non-linear market behavior

---

### Random Forest
Generally produced more flexible predictions.

Strength:
- Captures complex feature interactions
- Better handling of market non-linearity

---

### Important Predictive Features
Most influential features included:

- Open price
- High price
- Moving averages
- Price range

---

### Stock Market Predictability
Short-term stock prices exhibit patterns but remain noisy due to market volatility.

---

## Conclusion
Both regression models successfully predicted short-term stock price movement trends.

Random Forest generally performs better due to its ability to model non-linear relationships, while Linear Regression serves as a strong interpretable baseline.

This project demonstrates how historical financial indicators and feature engineering can be used for practical stock forecasting using machine learning.