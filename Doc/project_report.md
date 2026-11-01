# Retail Sales Analytics & Demand Forecasting
## Detailed Project Report

### 1. Introduction

This project focuses on retail transaction analytics and weekly demand forecasting using the Dunnhumby Let's Get Sort-of-Real dataset.

The objective is to analyze historical retail sales, identify business patterns, and evaluate forecasting techniques.

### 2. Problem Statement

Retail businesses generate large volumes of transaction data. Extracting meaningful insights from these records can help understand product performance, customer behavior, store performance, and demand trends.

This project addresses these analytical requirements using Python, SQL, DuckDB, and Power BI.

### 3. Dataset Description

**Dataset:** Dunnhumby – Let's Get Sort-of-Real

**Historical period:** April 2006 – July 2008

**Transaction records:** Approximately 307.5 million rows.

Important attributes include:

- SHOP_DATE
- SHOP_WEEK
- QUANTITY
- SPEND
- PROD_CODE
- CUST_CODE
- BASKET_ID
- STORE_CODE
- STORE_FORMAT
- STORE_REGION

The dataset is synthetic retail transaction data.

### 4. Data Preparation and Quality Analysis

The data profiling stage examined:

- Missing values
- Data types
- Revenue and quantity distributions
- Customer identifier completeness
- Product and store identifiers
- Potential duplicate records

Customer identifiers were missing for a significant portion of transaction records. This limitation was considered during customer-level analysis.

### 5. Exploratory Data Analysis

The following analyses were performed:

1. Product-level sales analysis
2. Store-level performance analysis
3. Customer segment analysis
4. Basket analysis
5. Monthly revenue analysis
6. Quarterly revenue analysis
7. Yearly revenue analysis
8. Data visualization

### 6. SQL Analysis

DuckDB was used to perform analytical queries and generate aggregated datasets.

The SQL analysis included:

- Filtering and aggregation
- GROUP BY and HAVING
- Joins
- Common Table Expressions
- Subqueries
- Window functions
- Analytical views

The generated analytical views supported the Power BI reporting stage.

### 7. Power BI Dashboard

Three dashboard pages were developed.

#### 7.1 Sales Overview

Includes revenue KPIs, units sold, product analysis, customer segment analysis, and store format contribution.

#### 7.2 Store and Product Performance

Includes store-level and regional performance analysis, store format comparisons, and product visualizations.

#### 7.3 Sales Trends and Forecast

Includes monthly revenue trends, monthly units sold, average revenue per unit, and a built-in Power BI forecast visualization.

### 8. Weekly Demand Forecasting

Weekly revenue was aggregated from the original transaction CSV files and mapped to actual dates using the provided time mapping files.

**Total weekly observations:** 117

**Training observations:** 104 weeks

**Initial test observations:** 13 weeks

Forecasting approaches evaluated:

- Naive Baseline
- Holt Linear Trend
- Seasonal Naive
- Holt-Winters Exponential Smoothing

### 9. Model Evaluation

Rolling-origin validation was performed using four historical evaluation windows.

| Model | Average Rolling MAPE |
|---|---:|
| Seasonal Naive | 4.30% |
| Holt Linear | 6.49% |
| Naive Baseline | 7.39% |

Seasonal Naive achieved the lowest average rolling MAPE and was selected for the final benchmark forecast.

The model generates forecasts by repeating corresponding observations from the previous 52-week cycle.

### 10. Final Forecast

The selected model generated a 13-week forecast for:

**7 July 2008 – 29 September 2008**

The output was exported to:

`processed_data/final_weekly_demand_forecast.csv`

### 11. Key Findings

- Retail transaction data can be transformed into useful product, store, customer, and sales insights.
- Weekly aggregation provides more observations than the monthly forecasting dataset.
- Seasonal Naive outperformed the other evaluated models in average rolling validation.
- A more complex model does not necessarily provide better forecasting performance.
- Historical validation results should not be treated as guaranteed future accuracy.

### 12. Limitations

- The available historical period is limited.
- Four rolling validation windows provide only a preliminary evaluation.
- Seasonal Naive does not learn future growth or changing market conditions.
- Customer information contains missing values.
- Promotion uplift could not be evaluated without suitable promotion data.
- Additional external variables may improve forecasting performance.

### 13. Future Scope

- More extensive rolling-origin validation.
- Additional statistical and machine learning forecasting models.
- Product-level and store-level demand forecasting.
- Integration of promotional and pricing data.
- Automated reporting and monitoring.

### 14. Conclusion

The project demonstrates an end-to-end retail analytics workflow covering data profiling, exploratory analysis, SQL-based data processing, interactive Power BI reporting, and weekly demand forecasting.

The forecasting experiments demonstrate the importance of evaluating models against simple baselines and using time-aware validation before selecting a model.

### 15. Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn
- DuckDB
- SQL
- Power BI
- Jupyter Notebook

### 16. Dataset Reference

Dunnhumby – Let's Get Sort-of-Real dataset.

Original dataset documentation and source information should be linked here.