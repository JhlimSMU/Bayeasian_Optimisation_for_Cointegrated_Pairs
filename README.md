# Bayesian Optimization for Cointegrated Pairs

## 📌 Overview
This project implements a **cointegration-based pairs trading strategy** enhanced with **Bayesian Optimization**. The framework identifies cointegrated asset pairs, constructs spreads, and optimizes trading parameters to maximize **risk-adjusted returns** while controlling drawdowns and turnover.

## ⚙️ Methodology
- **Pair Selection:** Engle-Granger & Johansen tests to identify cointegrated pairs.  
- **Spread Construction:** OLS/Johansen eigenvector hedge ratio.  
- **Signal Generation:** Rolling z-score of spreads with entry/exit thresholds.  
- **Bayesian Optimization:** Gaussian Process with Expected Improvement to tune:  
  - Entry/exit thresholds  
  - Lookback window  
  - Stop-loss & timeout rules  
  - Hedge ratios  
- **Validation:** Rolling walk-forward out-of-sample testing.  
- **Risk Controls:** Max exposure per pair, sector caps, and transaction cost modeling.  

## 📊 Results
- Robust **out-of-sample Sharpe** compared to fixed-rule benchmarks.  
- Reduced drawdowns and stable cumulative PnL across multiple market regimes.  
- Visualization outputs:  
  - Equity curve & drawdown plots  
  - Parameter convergence  
  - Pair selection diagnostics  

## 🛠️ Requirements
- Python 3.9+  
- Jupyter Notebook  
- Libraries: `pandas`, `numpy`, `statsmodels`, `scikit-learn`, `matplotlib`, `bayesian-optimization`  

Install dependencies:
```bash
pip install -r requirements.txt

