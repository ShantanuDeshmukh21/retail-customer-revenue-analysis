# Retail Customer & Revenue Analysis

## View the Notebook
> GitHub's notebook renderer can be unreliable. Use the links below for the best experience:

[![Open in nbviewer](https://img.shields.io/badge/Open%20in-nbviewer-orange?logo=jupyter)](https://nbviewer.org/github/ShantanuDeshmukh21/retail-customer-revenue-analysis/blob/master/retail_analysis.ipynb)

## Overview
End-to-end SQL and Python analysis of 500 customers, 50 products, and 3,000+ retail transactions across 2023–2024. Identifies revenue concentration, customer loyalty patterns, seasonal trends, and top-performing product categories.

## Business Questions Answered
1. Pareto Analysis — do top 20% of customers drive 80%+ of revenue?
2. Repeat Purchase Rate — loyal vs. one-time buyers and the revenue difference
3. Seasonal Trends — monthly and quarterly revenue patterns (Q4 holiday effect)
4. Category Performance — which product categories generate the most revenue
5. Top Customer Ranking — using SQL window functions (RANK, NTILE, running totals)

## Tech Stack
| Tool | Purpose |
|------|---------|
| Python (Pandas, NumPy) | Data generation and manipulation |
| SQLite (sqlite3) | In-memory SQL query execution |
| Matplotlib, Seaborn | Data visualization |
| Jupyter Notebook | Interactive analysis environment |

## Key SQL Concepts Demonstrated
- `NTILE()` — customer quintile bucketing for Pareto analysis
- `RANK() OVER (PARTITION BY ...)` — city-level customer ranking
- `SUM() OVER ()` — running totals and percentage-of-total calculations
- Multi-table JOINs (customers → orders → order_items)
- CTEs (Common Table Expressions) for readable query structure

## Key Findings
- Top 20% of customers account for the large majority of total revenue
- Loyal customers (5+ orders) have a significantly higher lifetime value than one-time buyers
- Q4 (Oct–Dec) is the peak revenue period — holiday demand is clearly visible in the data
- Electronics is the highest-revenue product category

## How to Run
1. Open `retail_analysis.ipynb` in Jupyter Notebook or JupyterLab
2. Run all cells: Kernel → Restart & Run All
3. Charts render inline and are saved as .png files in this folder

## Output Charts
- `pareto_analysis.png` — Revenue concentration and cumulative Pareto curve
- `repeat_purchase.png` — Buyer segment comparison by count and lifetime value
- `monthly_trends.png` — Monthly and quarterly revenue (2023 vs 2024)
- `category_performance.png` — Revenue and avg transaction value by category
- `top10_customers.png` — Top 10 customers ranked by lifetime value

---
*Author: Shantanu Deshmukh | MS Computer Science, NJIT*
