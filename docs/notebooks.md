# Notebooks Guide

Use notebooks for exploration, modeling, and reporting; keep production code in `src/`. Notebooks are central to this project for EDA, forecasting, and portfolio analysis.

## Typical Flow

1. **Task 1: Data Preprocessing and Exploration**
   - Load and profile raw financial data from YFinance.
   - Clean data, handle missing values, and perform time-based indexing.
   - Conduct EDA: Visualize closing prices, calculate daily returns, analyze volatility.
   - Test for stationarity (e.g., Augmented Dickey-Fuller test).
   - Calculate risk metrics (VaR, Sharpe Ratio).

2. **Task 2: Build Forecasting Models**
   - Prepare data for modeling (train/test split chronologically).
   - Implement ARIMA/SARIMA: Use ACF/PACF or auto_arima for parameters.
   - Implement LSTM: Prepare sequences, build and train the model.
   - Evaluate models using MAE, RMSE, MAPE.

3. **Task 3: Forecast Future Trends**
   - Generate forecasts (6-12 months) with confidence intervals.
   - Visualize forecasts alongside historical data.
   - Analyze trends, opportunities, and risks.

4. **Task 4: Portfolio Optimization**
   - Compute expected returns and covariance matrix.
   - Generate Efficient Frontier using PyPortfolioOpt.
   - Identify key portfolios (Max Sharpe, Min Volatility).
   - Recommend optimal weights.

5. **Task 5: Backtesting**
   - Define backtesting period and benchmark.
   - Simulate portfolio performance.
   - Compare against benchmark and analyze results.

## Practices

- Keep notebooks deterministic; set random seeds for reproducibility.
- Save generated figures and tables under `outputs/figures/`.
- Avoid side effects; move reusable code to `src/` and import.
- Document insights and justifications in markdown cells.

## Running

- Open notebooks in Jupyter Lab or VS Code.
- Ensure the virtual environment is active and dependencies installed.
- Execute cells top-to-bottom and commit meaningful results (e.g., plots, metrics).

Refer to the main README for project-specific commands.
