# Retail Sales Analytics & Demand Forecasting

An end-to-end retail data analytics project focused on analyzing large-scale retail transactions, identifying business insights, and evaluating weekly demand forecasting models.

## Project Overview

This project uses the Dunnhumby **Let's Get Sort-of-Real** dataset to perform retail sales analysis and demand forecasting.

The objective is to transform raw retail transaction data into meaningful business insights through Python, SQL, DuckDB, and Power BI.

The project covers data profiling, exploratory data analysis, SQL analytics, interactive dashboards, and time-series forecasting.

## Objectives

- Analyze overall retail sales and revenue trends.
- Identify top-performing products and stores.
- Understand customer segment behavior.
- Analyze store formats and regional performance.
- Study historical sales trends.
- Build and evaluate weekly demand forecasting models.
- Present business insights through interactive Power BI dashboards.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data processing, EDA and forecasting |
| Pandas & NumPy | Data manipulation |
| Matplotlib | Data visualization |
| Statsmodels | Time-series forecasting |
| Scikit-learn | Forecast evaluation |
| DuckDB | Analytical SQL queries |
| SQL | Data aggregation and analysis |
| Power BI | Interactive dashboards |
| Jupyter Notebook | Analysis and experimentation |

## Dataset Information

**Source:** Dunnhumby – Let's Get Sort-of-Real.

The dataset contains historical retail transaction records covering:

- 307 million+ transaction rows
- 494,880 unique customer codes
- 4,997 unique product codes
- Approximately 819 days of transaction history
- Historical period: April 2006 – July 2008

The dataset is synthetic retail data provided for analytical purposes. It does not represent actual transactions from a specific retail chain.

## Project Workflow

### 1. Data Profiling and Preparation
- Explored transaction CSV files.
- Examined data types and missing values.
- Performed data quality checks.
- Identified customer and product-level information.

### 2. Exploratory Data Analysis
- Product performance analysis.
- Store performance analysis.
- Customer segment analysis.
- Basket and sales analysis.
- Monthly, quarterly and yearly revenue trends.
- Data visualization using Python.

### 3. SQL Analytics
Used DuckDB for analytical queries and aggregations.

Key analytical areas:
- Product sales performance.
- Store-level revenue.
- Customer segment revenue.
- Monthly sales trends.
- SQL joins, CTEs and window functions.
- Analytical views for Power BI.

### 4. Power BI Dashboard

Three dashboard pages were developed:

**Page 1 – Sales Overview**
- Revenue KPIs
- Units sold
- Product performance
- Customer segment analysis
- Store format contribution

**Page 2 – Store & Product Performance**
- Store performance analysis
- Regional comparison
- Store format analysis
- Product performance visualizations

**Page 3 – Sales Trends & Forecast**
- Monthly revenue trends
- Monthly units sold
- Revenue forecasting visualization
- Average revenue per unit
- Monthly revenue movement

### 5. Weekly Demand Forecasting

Weekly revenue data was aggregated from the original transaction files.

Forecasting models evaluated:

- Naive Baseline
- Holt Linear Trend
- Seasonal Naive
- Holt-Winters Exponential Smoothing

Rolling-origin validation was used to compare model performance.

#### Model Comparison

| Model | Average Rolling MAPE |
|---|---:|
| Seasonal Naive | 4.30% |
| Holt Linear | 6.49% |
| Naive Baseline | 7.39% |

**Selected model: Seasonal Naive**

The selected model generated a 13-week forecast covering July to September 2008.

The 4.30% MAPE represents historical rolling validation performance, not a guarantee of future accuracy.

## Project Outputs

The processed outputs include:

- `weekly_sales_dataset.csv`
- `final_weekly_demand_forecast.csv`
- `weekly_model_comparison.csv`
- `rolling_validation_results.csv`

Additional outputs include processed analytical datasets, SQL views, Jupyter notebooks, and a Power BI report.

## Repository Structure

```text
Retail-Sales-Analytics/
│
├── Dataset/                     # Raw dataset (not committed)
│
├── processed_data/
│   ├── weekly_sales_dataset.csv
│   ├── final_weekly_demand_forecast.csv
│   ├── weekly_model_comparison.csv
│   └── rolling_validation_results.csv
│
├── powerbi_data/
│   └── Aggregated CSV datasets
│
├── docs/
│   └── PROJECT_REPORT.md
│
├── notebooks/
│   ├── profile_data.ipynb
│   └── demand_forecasting.ipynb
│
├── Retail_Analytics_Project.pbix
├── retail_analytics.duckdb
├── README.md
└── .gitignore
```

*Update the folder structure if your actual repository differs.*

## Limitations

- The historical dataset covers a limited time period.
- Customer identifiers and demographic segments contain missing values.
- The forecasting history is relatively short for robust long-term seasonal modelling.
- The selected Seasonal Naive model repeats corresponding historical weeks and does not independently learn future growth.
- Rolling validation performance may differ from actual future performance.
- Promotion uplift analysis was not performed because a suitable promotion dataset was not established.

## Future Improvements

- Evaluate additional forecasting models.
- Perform more extensive time-series cross-validation.
- Incorporate promotion and pricing information when available.
- Explore product-level demand forecasting.
- Develop automated reporting pipelines.
- Improve forecast monitoring and error analysis.

## How to Run

1. Clone the repository.
2. Install the required Python packages.
3. Open the Jupyter notebooks.
4. Configure the dataset path.
5. Execute the analysis and forecasting notebooks.
6. Open the Power BI report using Power BI Desktop.

## Disclaimer

This is an independent academic portfolio project developed for learning and analytical purposes.

Dataset source: Dunnhumby – Let's Get Sort-of-Real.

All analysis and interpretations are based on the available dataset.