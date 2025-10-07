# Crypto Price Analysis

This repository packages a **reproducible crypto price analysis** based on the included Jupyter notebook.  
It extracts and saves any charts generated in the notebook, and provides a clear project structure so you can publish it directly to GitHub.


## 🔎 Project Overview

The analysis explores historical market behavior for **BTC, DOGE, DOT** using Python data tools.  
Typical steps include:
- Data ingestion and cleaning
- Feature engineering for returns and rolling statistics
- Visualization of price levels, returns, moving averages, and risk
- Cross-asset relationships (e.g., correlations) and drawdown inspection
- (Optional) light forecasting or seasonal diagnostics

### Likely Topics Covered
- returns & volatility
- correlation analysis
- rolling metrics
- seasonality
- forecasting
- technical indicators



## 🧰 Environment & Setup

1. **Create a virtual environment (recommended)**  
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # Windows: .venv\Scripts\activate
   ```

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Open the notebook**  
   ```bash
   jupyter lab  # or: jupyter notebook
   ```

If your notebook depends on external data sources (e.g., APIs like `yfinance`), the runtime will fetch data when you run the cells.  
For fully offline reproducibility, consider exporting any fetched datasets to a `data/` folder and reading from disk.

## How to Reproduce the Figures

1. Open `notebooks/crypto-price-analysis.ipynb`.
2. Run the notebook **top to bottom**.
3. Ensure plotting cells display charts (e.g., `matplotlib.pyplot.show()` or Plotly display).
4. Commit the refreshed notebook and any newly exported images under `figures/`.

## Notes on Data & Assumptions

- Markets analyzed: **BTC, DOGE, DOT** (as detected from notebook text/code).
- Time horizon and sampling frequency depend on the data-loading cell(s) in your notebook.
- Return calculations (simple vs. log), moving-average windows, and risk metrics should be documented inline in the notebook for clarity.

## Future Enhancements

- Add a `src/` script to **batch-export** figures from the notebook using `nbconvert` for CI.
- Store parameters (tickers, date ranges, lookback windows) in a small `config.yaml`.
- Include **unit checks** on data integrity (missing values, duplicated timestamps).

---

**Author**: Your Name  
**License**: MIT (or your preferred license)

