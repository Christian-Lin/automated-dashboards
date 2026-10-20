# Sales Performance 2025

An interactive dashboard of 2025 sales: completed revenue, orders, average order value, gross margin, order outcomes and budget variance, from the cleaned `Sales_Data_v1` workbook (499 transactions across 30 products and 150 customers).

**Live page:** https://christian-lin.github.io/automated-dashboards/sales-performance-2025/

## What's here

- `index.html` – the whole dashboard in one self-contained file. d3 v7 loads from a CDN; the data is embedded in the page, so it needs no server or build step.
- `sales_transactions_2025.csv` – the transactions behind it, joined to each product's category, unit cost and stock status and each customer's region and loyalty tier (names and emails left out).
- `monthly_budget_2025.csv` – budget and actual revenue and orders per category per month.

## Features

- Filters for category, region, stock status and a month range; every card follows them, and Reset returns to the full year
- Headline figures: completed revenue, completed orders, average order value, gross margin, cancelled or returned share
- Completed revenue by month
- Budget vs actual by month, with the variance for each category over the chosen months
- Revenue by region (the chosen region is highlighted) and how orders ended
- Sortable product table
- Light and dark mode follow the system setting

## Data notes

- Revenue counts Completed orders only. Gross margin is (revenue − unit cost × quantity) ÷ revenue.
- Stock status is each product's current status from the Products tab, not its status when the order was placed.
- The budget tab's actuals come from a different source and run about 12× the transaction totals, so they're compared only with their own budget. Region and stock status don't apply to it.
- Cleaning before publishing: T-10077's quantity corrected from −2 to 5 and T-10233's discount from 150% to 15% (both match their totals exactly); the second T-10449 renamed T-10501; C-2120's region set to West; C-2042's invalid age cleared; order T-10310 (unknown customer C-9999) and placeholder product P-1031 removed.

To run locally, open `index.html` in a browser (an internet connection is needed for the CDN script).
