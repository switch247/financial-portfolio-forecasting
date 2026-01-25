# Business Understanding: Time Series Forecasting for Portfolio Management Optimization

## Business Objective
Guide Me in Finance (GMF) Investments is a forward-thinking financial advisory firm that specializes in personalized portfolio management. GMF leverages cutting-edge technology and data-driven insights to provide clients with tailored investment strategies. By integrating advanced time series forecasting models, GMF aims to predict market trends, optimize asset allocation, and enhance portfolio performance. The company's goal is to help clients achieve their financial objectives by minimizing risks and capitalizing on market opportunities.

The Efficient Market Hypothesis suggests that predicting exact stock prices using only historical price data is exceptionally difficult. Therefore, in an industry setting, these models are more often used to forecast volatility, identify momentum factors, or serve as one of many inputs into a larger decision-making framework, rather than for direct, standalone price prediction.

## Situational Overview (Business Need)
As a Financial Analyst at GMF Investments, your objective is to apply time series forecasting to historical financial data to enhance portfolio management strategies. Your role involves analyzing data, building predictive models, and recommending portfolio adjustments based on forecasted trends.

You will:
- Utilize YFinance data to extract historical financial information such as stock prices, market indices, and other relevant financial metrics.
- Preprocess and analyze this data to identify trends and patterns.
- Develop and evaluate forecasting models to predict future market movements.
- Use the insights gained to recommend changes to client portfolios that aim to optimize returns while managing risks.

## Data
Use historical financial data for three key assets sourced from the YFinance Python library covering the period from January 1, 2015 to January 15, 2026.

### Assets
- **Asset: Tesla (TSLA)** - High-growth stock in the consumer discretionary sector (Automobile Manufacturing) - Risk Profile: High risk, high potential return
- **Asset: Vanguard Total Bond Market ETF (BND)** - Tracks U.S. investment-grade bonds - Risk Profile: Low risk, stability and income
- **Asset: S&P 500 ETF (SPY)** - Tracks the S&P 500 Index - Risk Profile: Moderate risk, broad market exposure

### Data Fields
Each dataset includes:
- Date: Trading day timestamp
- Open, High, Low, Close: Daily price metrics
- Adj Close: Adjusted close price accounting for dividends and splits
- Volume: Total number of shares/units traded each day

### Usage in Portfolio Analysis
- TSLA provides potential high returns with high volatility
- BND contributes stability and low risk
- SPY offers diversified, moderate-risk market exposure

## Learning Outcomes
### Skills:
- API Usage: Skillfully fetching financial data from an API (yfinance)
- Data Wrangling: Using pandas for cleaning, handling missing dates/values, time-based indexing, and merging datasets
- Feature Engineering: Calculating daily returns, rolling volatility, and other relevant metrics
- Data Scaling: Applying normalization or standardization as preprocessing
- Statistical Modeling: Building, training, and optimizing ARIMA/SARIMA models using statsmodels and pmdarima
- Deep Learning Modeling: Constructing, training, and evaluating an LSTM model for time series forecasting
- Model Evaluation: Calculating and comparing performance metrics (MAE, RMSE, MAPE)
- Optimization & Visualization: Running simulations to generate and plot the Efficient Frontier
- MPT Implementation: Using libraries like PyPortfolioOpt
- Simulation: Implementing a simple backtesting loop to simulate portfolio performance

### Knowledge:
- Understanding the characteristics of different asset classes: high-growth stocks (TSLA), bonds for stability (BND), and market indices for diversification (SPY)
- Familiarity with the Efficient Market Hypothesis (EMH) and its practical implication that pure price prediction is difficult
- Deeply understanding what stationarity is, why it's crucial for models like ARIMA, and how to test for it
- Knowing what the Efficient Frontier represents and the significance of portfolios that lie on it
- Understanding the purpose and methodology of backtesting a financial strategy
- Knowing the importance of using a benchmark for objective performance evaluation

### Behaviors:
- Critical Evaluation: The ability to compare and contrast different modeling approaches
- Problem Framing & Synthesis: The ability to translate a high-level business objective into technical requirements
- Data-Driven Decision Making: Making recommendations grounded in evidence

### Communication:
- Writing professional investment memos for non-technical stakeholders
- Presenting model comparisons with clear justifications

## Team
- Tutors: Kerod, Mahbubah, Filimon, Smegnsh

## Key Dates
- Challenge Introduction: 10:30 AM UTC on Wednesday, 21 Jan 2026
- Interim Submission: 8:00 PM UTC on Sunday, 25 Jan 2026
- Final Submission: 8:00 PM UTC on Tuesday, 27 Jan 2026

## Communication & Support
- Slack channel: #all-week9
- Office hours: Mon–Fri, 08:00–15:00 UTC

For a detailed breakdown of tasks and deliverables, see `experiments/todo.md`.
