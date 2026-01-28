# Time Series Forecasting for Portfolio Management Optimization

This project implements time series forecasting models to enhance portfolio management strategies for Guide Me in Finance (GMF) Investments. By leveraging historical financial data from key assets, the project aims to predict market trends, optimize asset allocation, and improve portfolio performance while managing risks.

## Business Objective
GMF Investments specializes in personalized portfolio management using data-driven insights. This project applies advanced time series forecasting to historical financial data to predict market movements and recommend portfolio adjustments. It incorporates the Efficient Market Hypothesis, recognizing that pure price prediction is challenging, and focuses on volatility forecasting, momentum factors, and integration into broader decision-making frameworks.

As a Financial Analyst at GMF, the goal is to:
- Extract and analyze historical data from YFinance for TSLA, BND, and SPY.
- Build and evaluate forecasting models (ARIMA/SARIMA and LSTM).
- Generate future forecasts and use them for portfolio optimization via Modern Portfolio Theory (MPT).
- Backtest the strategy against benchmarks to validate performance.

## Assets and Data
- **Assets:**
  - **TSLA (Tesla):** High-growth stock in consumer discretionary sector (Automobile Manufacturing) – High risk, high potential return.
  - **BND (Vanguard Total Bond Market ETF):** Tracks U.S. investment-grade bonds – Low risk, stability and income.
  - **SPY (S&P 500 ETF):** Tracks the S&P 500 Index – Moderate risk, broad market exposure.
- **Data Period:** January 1, 2015, to January 15, 2026.
- **Data Fields:** Date, Open, High, Low, Close, Adj Close, Volume.
- **Source:** YFinance Python library.

## Project Tasks
1. **Preprocess and Explore the Data:** ✅ Extract data, clean it, perform EDA, check stationarity, calculate risk metrics (VaR, Sharpe Ratio), and visualize trends.
2. **Build Time Series Forecasting Models:** ✅ Implement ARIMA/SARIMA and LSTM models, optimize parameters, and evaluate using MAE, RMSE, MAPE.
3. **Forecast Future Market Trends:** ✅ Generate 6-12 month forecasts with confidence intervals, analyze trends, and assess opportunities/risks.
4. **Optimize Portfolio Based on Forecast:** ✅ Use MPT to compute expected returns, covariance matrix, and generate the Efficient Frontier. Recommend optimal portfolios (e.g., Maximum Sharpe Ratio, Minimum Volatility).
5. **Strategy Backtesting:** ✅ Simulate portfolio performance over a historical period (e.g., Jan 2025 - Jan 2026) and compare against a benchmark (e.g., 60% SPY / 40% BND).

## Current Status
All tasks (1-5) have been completed. The project includes fully implemented notebooks for EDA, time series forecasting, future trend forecasting, portfolio optimization, and strategy backtesting. Key deliverables include trained models, forecasts, efficient frontier visualizations, portfolio recommendations, and backtesting results with performance metrics.

## Project Structure
```
portfolio-optimization/
├── config/                 # Configuration files (logging, settings)
├── data/
│   ├── processed/          # Cleaned and processed data
│   └── raw/                # Raw data (images, telegram messages - legacy)
├── docs/                   # Documentation
│   ├── business_understanding.md
│   ├── dependencies.md
│   ├── notebooks.md
│   └── README.md
├── experiments/
│   └── todo.md             # Challenge details and tasks
├── notebooks/              # Jupyter notebooks for EDA, modeling, and analysis
├── outputs/
│   ├── figures/            # Generated plots and visualizations
│   └── models/             # Saved trained models
├── reports/
│   ├── final.md            # Final report (Investment Memo)
│   └── interim.md          # Interim report
├── scripts/                # Python scripts for data processing, training, etc.
├── src/                    # Source code modules
│   ├── analysis/           # Correlation, hypothesis testing
│   ├── api/                # FastAPI for serving analytics (if applicable)
│   ├── config/             # Constants, logger, settings
│   ├── features/           # Feature engineering (scrapers, YOLO - legacy)
│   ├── pipeline/           # Modeling utilities, preprocessing, RAG, etc.
│   └── utils/              # Helpers for data loading, metrics, plotting
├── tests/                  # Unit tests
├── docker-compose.yml      # Docker setup
├── Dockerfile              # Containerization
├── dvc.yaml                # Data Version Control
├── Makefile                # Build automation
├── pyproject.toml          # Project dependencies and config
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

## Technologies and Libraries
- **Data Extraction:** yfinance
- **Data Processing:** pandas, numpy
- **Statistical Modeling:** statsmodels, pmdarima (for ARIMA/SARIMA)
- **Deep Learning:** TensorFlow/Keras (for LSTM)
- **Portfolio Optimization:** PyPortfolioOpt, scipy
- **Visualization:** matplotlib, seaborn, plotly
- **Testing:** pytest
- **Version Control:** Git, DVC
- **Containerization:** Docker
- **Orchestration:** Makefile, potentially Dagster (legacy)

## How to Run
1. **Set up Environment:**
   - Clone the repository and navigate to the project directory.
   - Install dependencies: `pip install -r requirements.txt` or use `pyproject.toml`.
   - Set up virtual environment if needed (see `scripts/setup_venv.ps1`).

2. **Data Extraction and Preprocessing:**
   - Run scripts in `scripts/` for data loading and preprocessing (e.g., `python scripts/load_telegram_messages.py` - adapt for financial data).
   - Use notebooks in `notebooks/` for EDA and model building.

3. **Modeling and Forecasting:**
   - Execute notebooks for ARIMA/SARIMA and LSTM implementation.
   - Train models and generate forecasts.

4. **Portfolio Optimization:**
   - Use PyPortfolioOpt to compute Efficient Frontier and optimal weights.

5. **Backtesting:**
   - Run simulation scripts to backtest the strategy.

6. **Reports and Visualizations:**
   - Generate plots in `outputs/figures/`.
   - Review reports in `reports/` for interim and final submissions.

For detailed API usage (if applicable), see `src/api/README.md`. For pipeline orchestration, refer to `scripts/README.md`.

## Documentation
- **Business Understanding:** `docs/business_understanding.md`
- **Dependencies:** `docs/dependencies.md`
- **Notebooks Guide:** `docs/notebooks.md`
- **Challenge Details:** `experiments/todo.md`
- **Reports:** `reports/interim.md` and `reports/final.md`

## Key Deliverables
- Jupyter notebooks with EDA, modeling, and analysis.
- Trained models and forecasts with visualizations.
- Efficient Frontier plots and portfolio recommendations.
- Backtesting results and performance metrics.
- Final Investment Memo (in `reports/final.md`).

## References
- Time Series Forecasting: ARIMA, LSTM tutorials from DataCamp, Machine Learning Mastery.
- Portfolio Optimization: PyPortfolioOpt documentation, MPT guides.
- Backtesting: QuantStart resources.

---
For more details on the challenge, see `experiments/todo.md`. This project is part of the 10 Academy AI Mastery Week 9 Challenge (Jan 21-27, 2026).

