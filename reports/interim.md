Interim Report: Time Series Forecasting for Portfolio Management Optimization

Date: January 26, 2026

Client: Guide Me in Finance (GMF) Investments

Subject: Analysis of TSLA, BND, and SPY for Optimized Asset Allocation

1. Understanding and Defining the Business Objective

Guide Me in Finance (GMF) Investments aims to revolutionize personalized portfolio management by integrating data-driven insights and advanced time series forecasting. The primary business objective is to provide clients with tailored investment strategies that maximize returns while minimizing risk.

However, the firm acknowledges the Efficient Market Hypothesis (EMH), which suggests that stock prices reflect all available information, making standalone price prediction challenging. Consequently, GMF’s objective is not merely to "time the market" but to:

Identify Momentum and Trends: Distinguish between noise and actionable market signals.

Forecast Volatility: Use predictive models to anticipate periods of high risk, allowing for proactive portfolio rebalancing.

Optimize Asset Allocation: Transition from static "60/40" models to dynamic, predictive frameworks using TSLA (High Growth), BND (Stability), and SPY (Market Proxy).

By integrating these forecasts into the Efficient Frontier framework, GMF ensures that investment strategies are based on the latest quantitative evidence rather than historical intuition alone.

2. Discussion of Completed Work and Initial Analysis

2.1 Data Preprocessing and Cleaning

We successfully extracted historical data using the yfinance API for the period January 5, 2015, to January 14, 2026. The data was cleaned by handling non-trading days and verifying adjusted close prices. All three assets were aligned to a common timeline to ensure that correlation and risk metrics were calculated on synchronous data points.

2.2 Exploratory Data Analysis (EDA) and Technical Validation

Initial analysis revealed significant disparities between the assets:

TSLA: High-growth, high-volatility. With an annualized volatility of 0.577 and a maximum drawdown of -73.6%, it represents the "engine" of growth but the primary source of risk.

BND: Acts as the "anchor." Its low volatility (0.054) and steady performance provide the necessary buffer against equity market shocks.

SPY: Represents the broader market. It offers a balanced risk-return profile (Sharpe Ratio 0.691).

Fundamental Concepts: Stationarity and the ADF Test

For time series models like ARIMA to be effective, the data must be stationary—meaning its statistical properties (mean, variance) do not change over time. To verify this, we utilized the Augmented Dickey-Fuller (ADF) Test.

Findings: Raw price data for all assets were non-stationary (p-values > 0.05). However, after applying first-differencing to calculate daily returns, all series became stationary (p-values < 0.01), satisfying the requirements for ARIMA modeling.

2.3 Key Figures and Analytical Support

Figure 1: Asset Price Comparison

[asset_price_comparison.png]
Description: A normalized comparison of TSLA, BND, and SPY price growth. Visually, it confirms the massive return disparity between Tesla and the broader market, supporting the need for a diversified portfolio.

Figure 2: Daily Percentage Change Comparison

[tsla_daily_returns_distribution.png]
Description: This time series plot of daily percentage changes across the three assets highlights the contrast in return magnitude. While BND and SPY show tight bounds, TSLA exhibits frequent spikes exceeding ±10%, visually justifying the need for robust risk management.

Figure 3: Risk Metrics Comparison

[risk_metrics_comparison.png]
Description: Comparison of Annualized Volatility and Sharpe Ratios. This confirms BND’s role as a strategic hedge due to its superior risk-adjusted return profile.

Figure 4: Rolling Statistics (Mean and Standard Deviation)

[tsla_30_day_rolling_volatility_annualized.png]
Description: This figure tracks the 30-day rolling mean alongside the rolling standard deviation. By visualizing both, we observe how the average return and the risk (volatility) evolve together. The spikes in rolling standard deviation coincide with periods of "volatility clustering," proving that risk is not constant and must be modeled dynamically.

Figure 5: Model Comparison Tesla Forecast

[model_comparison_tesla_forecast.png]
Description: Overlaid comparison of Actual TSLA prices vs. ARIMA and LSTM predicted values. This validates the selection of deep learning, as the LSTM tracks market turning points more effectively than the ARIMA model.

2.4 Time Series Forecasting Results

ARIMA (Baseline): Selection was based on ACF/PACF analysis. While mathematically sound for short-term trends, the model exhibited lag during volatility spikes.

LSTM (Deep Learning): Achieved lower error metrics (MAE/RMSE). Its ability to retain long-term dependencies makes it the primary input for the optimization phase.

3. Remaining Steps and Next Steps

3.1 Completion of Task 2: Model Refinement and Final Evaluation

To finalize the forecasting phase, we will focus on the following technical refinements:

Hyperparameter Tuning: Conduct a grid search for ARIMA orders $(p, d, q)$ and optimize LSTM architecture (hidden layers, dropout rate, and learning rate) to minimize the Root Mean Squared Error (RMSE).

Residual Analysis: Perform Ljung-Box tests on model residuals to ensure no autocorrelation remains, confirming that the models have captured all available signal.

Detailed Model Comparison: Produce a comprehensive comparison table including MAE, RMSE, and MAPE metrics across different time horizons to quantify the specific advantages of the LSTM approach over the ARIMA baseline.

3.2 Task 3: Forecast-Driven Portfolio Optimization

6-12 Month Forecasts: Extend the current short-term predictions to provide a 6-12 month outlook. This involves recursive forecasting and trend analysis to support long-term capital allocation decisions.

Confidence Intervals: Generate forecasts with 95% confidence intervals using bootstrapping for LSTM or standard errors for ARIMA to provide a range of probable outcomes.

Portfolio Rebalancing Simulation: Use predicted returns to determine optimal rebalancing frequencies (e.g., monthly vs. quarterly) to capture momentum while minimizing transaction costs.

3.3 Task 4: Development of AI-Driven Investment Dashboard

Portfolio Identification: Explicitly identify and visualize two key portfolio types:

Maximum Sharpe Ratio Portfolio: The tangency portfolio that offers the highest excess return per unit of risk.

Minimum Volatility Portfolio: The portfolio with the lowest possible variance, designed for conservative GMF clients.

Priority: Ensure low-latency predictions by optimizing the LSTM inference engine for real-time dashboard interaction.

Backtesting Strategy: Compare the optimized strategy against a 60/40 benchmark over a 2-year out-of-sample period (2024–2026).

4. Report Summary

The preliminary phase has established a robust data pipeline and validated that LSTM-based forecasting is significantly more effective for high-volatility assets. Moving forward, we will prioritize long-term (6-12 month) trend analysis and the identification of the Maximum Sharpe Ratio portfolio. This will ensure that GMF’s clients receive a balance of sophisticated deep-learning predictions and grounded, classical portfolio theory.

End of Interim Report