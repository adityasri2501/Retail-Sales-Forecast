# Retail Sales Forecast

A retail analytics and forecasting project focused on understanding sales performance, customer behavior, and product/store trends through data processing, analysis, and a Power BI dashboard.

## Overview

This repository contains a collection of retail transaction and customer data, processed analytical datasets, and a Power BI project for exploring sales patterns and forecasting opportunities. The project is designed to support data-driven decision-making for revenue planning, customer segmentation, and operational insights.

## Business Goal

The project aims to:

- analyze monthly, quarterly, and yearly sales trends
- evaluate store and product performance
- identify customer segments and purchasing behaviors
- assess missing/anonymized customer data quality
- support business reporting through a Power BI dashboard

## Repository Structure

```text
Retail-Sales-Forecast/
├── .gitignore
├── Retail_Analytics_Project.pbix
├── anonymous_customer_analysis.csv
├── complete_missing_value_audit.csv
├── profile_data.ipynb
├── retail_analytics.duckdb
├── transaction_profile.csv
├── processed_data/
│   ├── customer_segment_analysis.csv
│   ├── monthly_sales.csv
│   ├── product_analysis.csv
│   ├── quarterly_sales.csv
│   ├── store_analysis.csv
│   └── yearly_sales.csv
├── powerbi_data/
│   ├── vw_customer_segments.csv
│   ├── vw_monthly_sales.csv
│   ├── vw_product_sales.csv
│   └── vw_store_sales.csv
└── README.md
```

## Key Files

### Power BI Dashboard
- `Retail_Analytics_Project.pbix` — the main business intelligence dashboard for retail analytics and sales exploration.

### Notebook
- `profile_data.ipynb` — exploratory data analysis and profiling notebook used to understand the dataset structure, nulls, distributions, and patterns.

### Core Data Files
- `anonymous_customer_analysis.csv` — audit of customer anonymization and missing customer coverage across transaction files.
- `complete_missing_value_audit.csv` — summary of missing-value checks and data quality findings.
- `transaction_profile.csv` — profile summary of transactional data characteristics.
- `retail_analytics.duckdb` — DuckDB database file containing structured analytical data.

### Processed Analytical Outputs
The `processed_data/` folder includes cleaned and aggregated datasets used for reporting and trend analysis:

- `monthly_sales.csv` — monthly revenue/unit trends
- `quarterly_sales.csv` — quarterly summaries
- `yearly_sales.csv` — annual rollups
- `product_analysis.csv` — product-level performance analysis
- `store_analysis.csv` — store-level performance analysis
- `customer_segment_analysis.csv` — segmentation analysis

### Power BI Views
The `powerbi_data/` folder contains view-style exports that appear to be ready for dashboard consumption:

- `vw_monthly_sales.csv`
- `vw_product_sales.csv`
- `vw_store_sales.csv`
- `vw_customer_segments.csv`

## Data Characteristics

The repository appears to be built around retail transaction-level sales data spanning multiple months and years, with emphasis on:

- revenue and unit sales
- product performance
- store-level profitability/productivity
- customer segmentation
- anonymized customer tracking
- missing data quality assessment

## Suggested Workflow

1. Open `profile_data.ipynb` to inspect and profile the raw dataset.
2. Review the processed CSV files in `processed_data/` for cleaned analytics tables.
3. Open `Retail_Analytics_Project.pbix` to explore the dashboard and visual insights.
4. Use the CSV files in `powerbi_data/` for tabular data sources or reporting pipelines.

## Tools and Technologies

- Python / Jupyter Notebook
- Pandas and data profiling workflows
- DuckDB for analytical querying
- Power BI for dashboarding and business reporting

## Notes

This project is a strong example of end-to-end retail analytics: data profiling, cleaning, feature preparation, aggregation, and business reporting. It is suitable for showcasing analytical storytelling, KPI monitoring, and sales forecasting workflows.

## License

This repository does not include an explicit license file. If you plan to reuse or share the project publicly, consider adding a license that matches your intended usage.

## Contact

For questions or collaboration opportunities, please reach out via the repository owner or project contact information associated with this GitHub profile.
