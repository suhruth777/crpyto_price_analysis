## 🔍 Project Overview

This project performs an in-depth analysis of historical cryptocurrency price movements using Python-based data science tools.  
The goal is to uncover **patterns, risk factors, and market dynamics** that influence digital asset performance across time.

The analysis integrates:
- **Descriptive analytics** — understanding trends, volatility, and correlations
- **Technical analysis** — applying moving averages, RSI, MACD, and Bollinger Bands
- **Predictive analytics** — exploring models like ARIMA, Prophet, or XGBoost regressors
- **Comparative analysis** — contrasting Bitcoin, Ethereum, and other altcoins
- **Visualization** — clear graphical storytelling of trends, returns, and relationships

## 💾 Data Sources and Preparation

Data is primarily sourced via **Yahoo Finance (`yfinance`)**, ensuring accurate and up-to-date price and volume information.  
Each asset’s historical dataset includes:

| Field | Description |
|-------|--------------|
| `Date` | Daily timestamp |
| `Open` | Opening price |
| `High` | Highest price of the day |
| `Low` | Lowest price of the day |
| `Close` | Closing price |
| `Adj Close` | Adjusted closing price after splits/dividends |
| `Volume` | Trading volume |

### 🧹 Cleaning & Processing Steps
1. Converted timestamps to `datetime` objects and aligned indexes across tickers.
2. Removed missing data and resampled inconsistent date ranges.
3. Calculated daily returns (`pct_change()`), cumulative returns, and rolling volatility.
4. Engineered features for moving averages, RSI, and other technical indicators.
5. Normalized price scales for multi-asset comparisons.


## 📊 Analytical Insights

### 1️⃣ Descriptive Statistics
- Bitcoin (BTC) exhibits the **highest long-term return**, but also the greatest volatility.
- Ethereum (ETH) tends to show **strong correlation** with BTC (>0.8 in most windows).
- Altcoins like ADA and SOL display higher beta (amplified moves in both directions).

### 2️⃣ Moving Averages and Momentum
- Short-term moving averages (10–20 days) provide early but noisy signals.
- Long-term averages (50–200 days) capture structural trends with fewer false positives.
- The **Golden Cross / Death Cross** points show momentum reversals across assets.

### 3️⃣ Volatility & Risk
- Annualized volatility calculated via 30-day rolling windows highlights **clustered volatility** (volatility begets volatility).
- Drawdown plots reveal how long recovery periods differ by asset — BTC typically recovers faster than smaller altcoins.

### 4️⃣ Correlation Analysis
- Pairwise correlation matrices visualize how diversification potential shifts over time.
- During bull markets, correlations increase across assets (reduced diversification benefits).

### 5️⃣ Forecasting (Optional Section)
- ARIMA and Prophet models forecast future closing prices.
- Model performance measured by **MAE** and **RMSE** shows that simple models can track broad trends but fail to anticipate short-term shocks.


## 🧠 Key Takeaways

- **Crypto remains highly volatile**, but predictable patterns exist in rolling statistics and correlations.
- **Market synchronization** increases during large macro events — crypto assets tend to move together under stress.
- **Technical indicators** can improve decision-making but should be validated statistically, not visually.
- **Machine learning approaches** (e.g., XGBoost, LSTM) outperform naive models only when tuned on long-term data and sufficient features.

Overall, the analysis emphasizes the value of combining *technical indicators* with *quantitative risk metrics* rather than relying solely on price action.


## 🧮 Methods and Tools

| Category | Tools / Techniques |
|-----------|--------------------|
| Data Wrangling | `pandas`, `numpy` |
| Visualization | `matplotlib`, `seaborn`, `plotly` |
| Statistics | `statsmodels`, `scikit-learn` |
| Machine Learning | `XGBoost`, `TensorFlow` (for deep learning forecasts) |
| Feature Engineering | RSI, MACD, Bollinger Bands, Moving Averages |
| Time Series | Rolling metrics, ARIMA/Prophet models |


