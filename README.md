# Retail Sales Analytics & Demand Forecasting

An end-to-end retail analytics project using the Dunnhumby "Let's Get Sort-of-Real" dataset.

## Project Overview

This project analyzes large-scale retail transaction data to identify sales trends, product performance, customer segments, store performance, and future demand patterns.

## Tech Stack

- Python — Pandas, NumPy, Matplotlib, Statsmodels, Scikit-learn
- SQL — DuckDB
- Power BI — Interactive dashboards and visual analytics
- Jupyter Notebook — Data analysis and forecasting

## Project Workflow

1. Data cleaning and quality assessment
2. Exploratory Data Analysis (EDA)
3. SQL-based analytical queries
4. Power BI dashboard development
5. Weekly sales aggregation
6. Forecasting model comparison and validation

## Forecasting Results

Three weekly forecasting approaches were evaluated using rolling validation:

| Model | Average Rolling MAPE |
|---|---:|
| Seasonal Naive | 4.30% |
| Holt Linear | 6.49% |
| Naive Baseline | 7.39% |

**Selected model:** Seasonal Naive.

The final forecast covers 13 weeks, from July 7 to September 29, 2008.

Note: Historical validation performance does not guarantee future accuracy.

## Project Outputs

- `final_weekly_demand_forecast.csv`
- `weekly_model_comparison.csv`
- `rolling_validation_results.csv`
- `weekly_sales_dataset.csv`

## Dataset

Source: Dunnhumby — Let's Get Sort-of-Real.

The dataset contains synthetic retail transaction data and is used for educational and analytical purposes.

## Disclaimer

This project is an independent academic portfolio project. It does not represent actual transactions from any specific retail chain.