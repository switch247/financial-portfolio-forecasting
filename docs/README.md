# Project Documentation

This directory contains reusable, professional documentation for the Time Series Forecasting for Portfolio Management Optimization project.

## Folder Structure

```
Time-Series-Forecasting-for-Portfolio-Management-Optimization/
├── config/                     # Configuration files (logging, settings)
├── data/
│   ├── processed/              # Cleaned and processed financial data
│   └── raw/                    # Raw data (legacy: images, telegram messages)
├── docs/
│   ├── README.md               # Reusable project docs (this file)
│   ├── business_understanding.md # Business objective and context
│   ├── dependencies.md         # Environment & tooling overview
│   └── notebooks.md            # Notebook workflow guidance
├── experiments/
│   └── todo.md                 # Challenge brief & references
├── notebooks/                  # Jupyter notebooks for EDA, modeling, forecasting
├── outputs/
│   ├── figures/                # Generated plots and visualizations
│   └── models/                 # Saved trained models
├── reports/
│   ├── final.md                # Final investment memo
│   └── interim.md              # Interim report
├── scripts/                    # Utility scripts for data processing, training
├── src/                        # Library code: analysis, pipeline, utils
├── tests/                      # Unit tests
├── dvc.yaml                    # Data pipeline definition
├── docker-compose.yml          # Local services
├── pyproject.toml              # Build & tooling config
├── requirements.txt            # Python dependencies
└── README.md                   # Project-specific overview
```

## How to Run (High Level)

- Set up a Python virtual environment.
- Install project dependencies from `requirements.txt`.
- Extract and preprocess financial data using YFinance.
- Run notebooks for EDA, model training, forecasting, and portfolio optimization.
- Execute scripts for backtesting and evaluation.
- Generate reports and visualizations.

See the main project README for copy-ready commands tailored to this repository.

## Conventions

- Keep project-specific details in the root `README.md`.
- Place reusable guidance and references under `docs/`.
- Prefer interpretable baselines first; add explainability for complex models.
- Record experiments and decisions for traceability.
