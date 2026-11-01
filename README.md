# Fintech Transaction Analysis

A Python and Jupyter Notebook project exploring transaction outcomes, revenue trends, payment-method contribution, and customer-level activity in a sample fintech dataset.

## Overview

The notebook follows a simple transaction-analysis workflow:

1. Load transaction records and parse transaction dates.
2. Separate successful transactions from failed transactions.
3. Calculate transaction KPIs.
4. Examine monthly revenue and month-over-month change.
5. Compare value by payment type and customer.
6. Group customers into revenue-based segments.

## Repository Contents

| File | Description |
| --- | --- |
| `transaction.csv` | Sample transaction dataset |
| `fintechanalysis.ipynb` | Data preparation, KPI calculations, analysis, and visualizations |

## Dataset

The included CSV contains 10 sample transaction records across January to March 2024: 8 marked `Success` and 2 marked `Failed`.

| Column | Description |
| --- | --- |
| `transaction_id` | Transaction identifier |
| `customer_id` | Customer identifier |
| `transaction_date` | Transaction date |
| `amount` | Transaction amount |
| `transaction_type` | Payment type, such as UPI, Card, or NetBanking |
| `status` | Transaction outcome |

## Analysis

The notebook filters successful transactions for the revenue-oriented calculations.

| Metric | Value in the included sample |
| --- | ---: |
| Successful transactions | 8 |
| Successful transaction value | 11,800 |
| Average successful transaction value | 1,475 |

It also includes:

- Monthly successful transaction value and month-over-month growth.
- Revenue contribution by transaction type.
- Top customers by successful transaction value.
- Low-, medium-, and high-value customer groups using quantile-based segmentation.

## Run Locally

Requires Python 3.9 or later.

```bash
git clone https://github.com/UmerTukdi/fintech-business-insights.git
cd fintech-business-insights

python -m venv .venv
```

Activate the environment:

```bash
# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate
```

Install dependencies and launch Jupyter:

```bash
pip install pandas matplotlib notebook
jupyter notebook
```

Open `fintechanalysis.ipynb` and run the notebook cells in order. Keep `transaction.csv` in the repository root.

## Scope and Data Note

This repository contains a small sample dataset for demonstrating analysis techniques. It is not connected to a live payment gateway or production financial data, and the sample results are not statistically representative of a fintech business.
