# CS 440/540 Machine Learning in Finance - Homework 2

This repository contains the solutions for Homework 2 of the CS 440/540 Machine Learning in Finance course. The project focuses on time series analysis, forecasting, and algorithmic trading strategies using various statistical models.

## 📂 Project Structure

- **`CS440-540_HW2.ipynb`**: The main Jupyter Notebook containing all the code, analysis, and visualizations.
- **`unemployment.xlsx`**: Dataset for Problem 1 (Turkish Unemployment Rate).
- **`unemployment_plot.png`**: Generated plot for unemployment analysis.
- **`unemployment_forecast.png`**: Forecast output for Problem 1.

## 🚀 Topics Covered

### 1. ARIMA Modeling (Turkish Unemployment Rate)
- **Goal:** Predict future unemployment rates using historical data.
- **Method:**
  - Stationarity check (ADF Test).
  - Optimal parameter selection via Grid Search.
  - **Result:** Best Model identified as `ARIMA(4, 2, 5)`.

### 2. Multivariate Time Series (Crypto Portfolio via VARMA)
- **Goal:** Predict returns of 6 major cryptocurrencies (BTC, ETH, LTC, SOL, AVAX, BNB) and build a weekly rebalanced portfolio.
- **Method:**
  - Data fetching via `yfinance` (2023-2025).
  - `VARMA(p,q)` modeling with Grid Search.
  - Strategy backtesting (Top 2 coins selection).
- **Result:** High Sharpe Ratio achieved with `VARMA(1, 1)`.

### 3. Volatility Prediction (GARCH)
- **Goal:** Forecast volatility of Apple (AAPL) stock.
- **Method:**
  - Log-returns calculation.
  - `GARCH(p,q)` model optimization.
  - Rolling forecast for variance prediction.
- **Result:** Evaluated using MSE and R2 metrics.

### 4. Pairs Trading (Cointegration)
- **Goal:** Implement a cointegration-based pairs trading strategy for SP500 stocks.
- **Method:**
  - Select stock pairs from SP500.
  - Perform Cointegration tests to find mean-reverting pairs.
  - Backtest the strategy with $100 capital per pair.
- **Result:** Reported average profit over all possible pairs during the test period.

## 🛠️ Libraries Used
- **Data Analysis:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Financial Data:** `yfinance`
- **Statistical Modeling:** `statsmodels` (ARIMA, VARMA, ADF), `arch` (GARCH)

## 📥 Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/muzaffercanan/Velum-2.git
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib statsmodels yfinance arch
   ```
3. Open the notebook:
   ```bash
   jupyter notebook CS440-540_HW2.ipynb
   ```

---
**Author:** Muzaffer Canan
