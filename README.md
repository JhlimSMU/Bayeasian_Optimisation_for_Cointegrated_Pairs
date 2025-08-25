# Bayesian Optimization & Machine Learning for Cointegrated Pairs  

## 📌 Overview  
This project develops a **cointegration-based pairs trading strategy** enhanced with **Bayesian Optimization** and **XGBoost forecasting**. The framework identifies cointegrated pairs, constructs spreads, and predicts future spread movements. It then optimizes entry/exit rules, hedge ratios, and stop-loss settings to maximize **risk-adjusted returns** while controlling drawdowns and turnover.  

## ⚙️ Methodology  
- **Pair Selection:** Engle-Granger & Johansen tests to identify cointegrated pairs.  
- **Spread Construction:** OLS/Johansen eigenvector hedge ratio.  
- **Feature Engineering:** SMA correlations, volatility ratios, half-life, Bollinger %, rolling beta, lead-lag features.  
- **Forecasting:** XGBoost model to predict next-day spread changes.  
- **Bayesian Optimization:** Gaussian Process (Expected Improvement) to tune trading rules:  
  - Entry/exit thresholds  
  - Lookback windows  
  - Stop-loss & timeout rules  
  - Hedge ratios  
- **Validation:** Rolling walk-forward out-of-sample testing to avoid lookahead bias.  
- **Risk Controls:** Max exposure per pair, sector diversification, and transaction cost modeling.  

## 📊 Results  
- **Annualized Return:** 19.8%  
- **Sharpe Ratio:** 2.53  
- **Max Drawdown:** 3%  
- **Key Insights:**  
  - ML-based approach outperformed buy-and-hold (Sharpe 1.71, MDD 8.5%) and trend-following (Sharpe -0.27).  
  - Diversification across 17 pairs reduced portfolio-level drawdown.  
- **Visual Outputs:**  
  - Equity curve & drawdown plots  
  - Forecast vs actual spread diagnostics  
  - Parameter convergence and pair selection timelines  

## 🛠️ Requirements  
- Python 3.9+  
- Jupyter Notebook  
- Libraries: `pandas`, `numpy`, `statsmodels`, `scikit-learn`, `xgboost`, `matplotlib`, `bayesian-optimization`  

Install dependencies:  
```bash
pip install -r requirements.txt
