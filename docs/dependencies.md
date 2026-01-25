# Dependencies & Environment

This project uses Python data science and financial modeling libraries. The exact versions are managed via `requirements.txt` and `pyproject.toml`.

## Installation (High Level)

1. Set up a Python virtual environment (e.g., using venv or conda).
2. Install dependencies: `pip install -r requirements.txt`.
3. For GPU support (optional for LSTM), ensure TensorFlow is installed with CUDA if applicable.

## Key Libraries

### Data Extraction and Processing
- yfinance: Fetch historical financial data from Yahoo Finance.
- pandas: Data manipulation and analysis.
- numpy: Numerical computations.

### Statistical and Time Series Modeling
- statsmodels: Statistical models, including ARIMA/SARIMA.
- pmdarima: Auto ARIMA for parameter selection.

### Deep Learning
- tensorflow: Deep learning framework for LSTM models.
- keras: High-level API for building neural networks.

### Portfolio Optimization
- PyPortfolioOpt: Tools for Modern Portfolio Theory, including Efficient Frontier calculation.

### Visualization
- matplotlib: Plotting and visualization.
- seaborn: Statistical data visualization.
- plotly: Interactive plots.

### Utilities
- scikit-learn: Machine learning utilities (e.g., preprocessing).
- scipy: Scientific computing for optimization.

### Testing and Development
- pytest: Unit testing.
- jupyter: Interactive notebooks.

## System/Service Dependencies
- Python 3.8+ recommended.
- Docker & Docker Compose (for containerized setup).
- Git for version control.
- DVC (Data Version Control) for data pipeline management.

## Other Tools
- Makefile: Automation of build and run tasks.
- VS Code or Jupyter Lab: For development and notebook execution.

See `requirements.txt` for the full list of Python dependencies.
- Prefer pinned versions for reproducibility.
- Use CI to validate installation and tests on push.
