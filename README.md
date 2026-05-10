# Personal Expense Tracker Visualization

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)

A Python-based personal finance project that ingests bank-style CSV data, stores transactions in SQLite, categorizes expenses with rule-based matching, generates visual reports, exports monthly Excel summaries, and provides an interactive Streamlit dashboard.

## Screenshots

### Streamlit Dashboard
![Streamlit Dashboard](screenshots/dashboard.png)

### Monthly Trend
![Monthly Trend](screenshots/monthly_trend.png)

### Category-wise Spending
![Category Bar Chart](screenshots/category_bar.png)

### Payment Method Split
![Payment Method Pie Chart](screenshots/payment_pie.png)

### Budget vs Actual
![Budget vs Actual](screenshots/budget_vs_actual.png)

## Project Overview

Personal Expense Tracker Visualization helps users analyze income, expenses, savings, category-wise spending, payment method usage, and monthly budget performance. The project is designed as a complete beginner-to-intermediate data analytics workflow using realistic personal finance data.

It includes:

- CSV ingestion and cleaning
- SQLite database storage
- Rule-based transaction categorization
- KPI calculations
- Matplotlib chart generation
- Excel report export
- Streamlit dashboard for interactive analysis

## Problem Statement

Personal expenses are often spread across cash, UPI, credit cards, and bank statements. Manually reviewing spending patterns can be slow and error-prone. This project solves that problem by creating a lightweight analytics pipeline that converts raw transaction data into useful summaries, charts, budget checks, and reports.

## Tech Stack

- **Python**: Core programming language
- **Pandas**: Data cleaning, aggregation, and reporting
- **SQLite**: Local transaction database
- **Matplotlib**: Static chart generation
- **Streamlit**: Interactive dashboard
- **XlsxWriter**: Excel report export

## Folder Structure

```text
Personal-Expense-Tracker-Visualization/
|-- data/
|   |-- expenses_sample.csv
|   `-- generate_sample.py
|-- db/
|   `-- expenses.db
|-- docs/
|-- images/
|-- notebooks/
|-- outputs/
|   |-- monthly_trend.png
|   |-- category_bar_2025-06.png
|   |-- payment_pie_2025-06.png
|   |-- daily_trend.png
|   `-- budget_vs_actual.png
|-- reports/
|   `-- expense_report_2025-06.xlsx
|-- screenshots/
|-- src/
|   |-- analyze.py
|   |-- app_streamlit.py
|   |-- budget.py
|   |-- categorize.py
|   |-- ingest.py
|   |-- models.py
|   |-- plots.py
|   `-- report.py
|-- tools/
|-- main.py
|-- requirements.txt
`-- README.md
```

## How To Run

Install dependencies:

```bash
pip install -r requirements.txt
```

Generate sample data:

```bash
python data/generate_sample.py
```

Run the full pipeline:

```bash
python main.py
```

This will:

- Initialize the SQLite database
- Ingest `data/expenses_sample.csv`
- Categorize transactions
- Generate PNG charts in `outputs/`
- Export an Excel report in `reports/`
- Print KPI summary in the terminal

Run the Streamlit dashboard:

```bash
streamlit run src/app_streamlit.py
```

Then open the local URL shown in the terminal, usually:

```text
http://localhost:8501
```

## Sample Output

Example transaction summary:

| Date       | Description              | Category          | Amount     | Account     |
|------------|--------------------------|-------------------|------------|-------------|
| 2025-01-01 | Monthly salary           | Income            | 85,000.00  | UPI         |
| 2025-01-03 | Swiggy order             | Food & Dining     | -650.00    | Credit Card |
| 2025-01-08 | Metro recharge           | Transport         | -500.00    | UPI         |
| 2025-01-12 | Amazon purchase          | Shopping          | -2,499.00  | Credit Card |
| 2025-01-18 | Electricity bill         | Bills & Utilities | -1,850.00  | UPI         |

Example KPI summary:

| Metric      | Value          |
|-------------|----------------|
| Total Spend | INR 328,972.10 |
| Income      | INR 660,527.95 |
| Savings     | INR 331,555.85 |

## Charts

The pipeline generates five PNG charts in the `outputs/` folder:

- **Monthly Trend**: Line chart showing total monthly spending.
- **Category Bar Chart**: Horizontal bar chart showing category-wise spending for a selected month.
- **Payment Method Pie Chart**: Pie chart comparing Cash, UPI, and Credit Card spending.
- **Daily Trend**: Area chart showing cumulative daily spending.
- **Budget vs Actual**: Grouped bar chart comparing monthly category budgets with actual spend.

## Streamlit Dashboard Features

- Sidebar filters for month and account
- KPI cards for total spend, income, and savings
- Category-wise spend chart
- Monthly trend chart
- Payment method split chart
- Budget check table with over-budget highlighting
- CSV upload and ingestion
- Manual transaction entry form

## Learning Outcomes

By completing this project, you practice:

- Designing a small analytics project structure
- Reading, cleaning, and standardizing CSV data with Pandas
- Creating and querying a SQLite database
- Applying rule-based text classification with regex
- Building reusable analysis functions
- Creating business-style charts with Matplotlib
- Exporting multi-sheet Excel reports
- Developing an interactive Streamlit dashboard
- Connecting data ingestion, analysis, visualization, and reporting into one pipeline

## Notes

The sample data is synthetic and covers January to June 2025. Expense amounts are negative, while income amounts are positive.