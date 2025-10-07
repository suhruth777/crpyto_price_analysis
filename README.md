# Crypto Price Analysis

This repository packages a **reproducible crypto price analysis** based on the included Jupyter notebook.  
It extracts and saves any charts generated in the notebook, and provides a clear project structure so you can publish it directly to GitHub.

## 📁 Repository Structure

```
crypto-price-analysis-repo/
├─ README.md
├─ requirements.txt
├─ .gitignore
├─ notebooks/
│  └─ crypto-price-analysis.ipynb
├─ figures/
│  ├─ figure_001.png
│  ├─ figure_002.png
│  └─ ...
└─ src/
   └─ (optional convenience scripts)
```

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

> If you update the notebook to add or remove sections, you can re-run the export cell (or this script) to refresh the **figures/** folder automatically.

## 🖼️ Key Results (Charts)

![Figure 1](figures/figure_001.png)
![Figure 2](figures/figure_002.png)
![Figure 3](figures/figure_003.png)
![Figure 4](figures/figure_004.png)
![Figure 5](figures/figure_005.png)
![Figure 6](figures/figure_006.png)
![Figure 7](figures/figure_007.png)
![Figure 8](figures/figure_008.png)
![Figure 9](figures/figure_009.png)
![Figure 10](figures/figure_010.png)
![Figure 11](figures/figure_011.png)
![Figure 12](figures/figure_012.png)
![Figure 13](figures/figure_013.png)
![Figure 14](figures/figure_014.png)
![Figure 15](figures/figure_015.png)
![Figure 16](figures/figure_016.png)
![Figure 17](figures/figure_017.png)
![Figure 18](figures/figure_018.png)
![Figure 19](figures/figure_019.png)
![Figure 20](figures/figure_020.png)
![Figure 21](figures/figure_021.png)
![Figure 22](figures/figure_022.png)
![Figure 23](figures/figure_023.png)
![Figure 24](figures/figure_024.png)
![Figure 25](figures/figure_025.png)
![Figure 26](figures/figure_026.png)
![Figure 27](figures/figure_027.png)
![Figure 28](figures/figure_028.png)
![Figure 29](figures/figure_029.png)
![Figure 30](figures/figure_030.png)
![Figure 31](figures/figure_031.png)
![Figure 32](figures/figure_032.png)
![Figure 33](figures/figure_033.png)
![Figure 34](figures/figure_034.png)
![Figure 35](figures/figure_035.png)
![Figure 36](figures/figure_036.png)
![Figure 37](figures/figure_037.png)
![Figure 38](figures/figure_038.png)
![Figure 39](figures/figure_039.png)
![Figure 40](figures/figure_040.png)
![Figure 41](figures/figure_041.png)
![Figure 42](figures/figure_042.png)
![Figure 43](figures/figure_043.png)
![Figure 44](figures/figure_044.png)
![Figure 45](figures/figure_045.png)
![Figure 46](figures/figure_046.png)
![Figure 47](figures/figure_047.png)
![Figure 48](figures/figure_048.png)
![Figure 49](figures/figure_049.png)
![Figure 50](figures/figure_050.png)
![Figure 51](figures/figure_051.png)
![Figure 52](figures/figure_052.png)
![Figure 53](figures/figure_053.png)
![Figure 54](figures/figure_054.png)
![Figure 55](figures/figure_055.png)
![Figure 56](figures/figure_056.png)
![Figure 57](figures/figure_057.png)
![Figure 58](figures/figure_058.png)
![Figure 59](figures/figure_059.png)
![Figure 60](figures/figure_060.png)
![Figure 61](figures/figure_061.png)
![Figure 62](figures/figure_062.png)
![Figure 63](figures/figure_063.png)
![Figure 64](figures/figure_064.png)
![Figure 65](figures/figure_065.png)
![Figure 66](figures/figure_066.png)

> The images above are extracted directly from the notebook’s outputs. If you don’t see a chart you expect, ensure that the relevant cell was executed and produced a PNG display before exporting.

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

## 🚀 How to Reproduce the Figures

1. Open `notebooks/crypto-price-analysis.ipynb`.
2. Run the notebook **top to bottom**.
3. Ensure plotting cells display charts (e.g., `matplotlib.pyplot.show()` or Plotly display).
4. Commit the refreshed notebook and any newly exported images under `figures/`.

## 📝 Notes on Data & Assumptions

- Markets analyzed: **BTC, DOGE, DOT** (as detected from notebook text/code).
- Time horizon and sampling frequency depend on the data-loading cell(s) in your notebook.
- Return calculations (simple vs. log), moving-average windows, and risk metrics should be documented inline in the notebook for clarity.

## 🏗️ Future Enhancements

- Add a `src/` script to **batch-export** figures from the notebook using `nbconvert` for CI.
- Store parameters (tickers, date ranges, lookback windows) in a small `config.yaml`.
- Include **unit checks** on data integrity (missing values, duplicated timestamps).

---

**Author**: Your Name  
**License**: MIT (or your preferred license)

