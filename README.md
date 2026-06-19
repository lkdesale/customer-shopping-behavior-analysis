- Retail Customer Shopping Behavior & Trends Analysis
An end-to-end data analytics project built on a retail customer shopping dataset, covering the full workflow from raw data to business recommendations: Python for data cleaning and feature engineering, SQL for relational modeling and business-question analysis, and Power BI for an interactive dashboard.

- Business Problem
A retail company wants to understand its customers' shopping behavior to improve sales, customer satisfaction, and long-term loyalty. This project answers:
"How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?"


- Tech Stack
Python (pandas, numpy) — data cleaning, feature engineering
SQL (SQLite) — star-schema data modeling, business-question queries
Power BI — interactive 4-page dashboard
Microsoft Word — project report

├── data/                  # Raw and cleaned datasets
├── python/                # Data cleaning & feature engineering scripts
├── sql/                   # Schema, queries, and SQLite database
├── powerbi/               # Power BI source tables, dashboard file, and build guide
├── report/                # Full project report (Word doc)
└── README.md

- Workflow
Data Preparation (Python) — Cleaned a 3,900-row retail dataset: standardized column names, imputed missing review ratings using category-wise medians, and engineered new features including age brackets, a composite customer value score, and a high-value customer flag. Also simulated purchase dates and an Online/Offline sales channel field to enable time-based and channel-based analysis.
Data Analysis (SQL) — Modeled the cleaned data into a star schema (dim_customers, dim_products, fact_transactions) in SQLite, and wrote 14 business-question queries covering channel performance, customer segmentation, loyalty drivers, and purchase drivers.
Visualization (Power BI) — Built a 4-page interactive dashboard: Overview (KPIs, revenue trend, channel split), Customer Segments, Loyalty & Repeat-Purchase Drivers, and Purchase Drivers — with slicers for season, channel, and category.
Report — A full written report summarizing methodology, key findings, and business recommendations, with embedded dashboard screenshots.


- Key Findings
Online dominates revenue: ~78% of orders and ~78% of revenue come from the Online channel — roughly 3.6x Offline.
Discounts show minimal impact: average order value and review rating are nearly identical whether a discount/promo was used or not, suggesting the current discounting strategy isn't a meaningful lever.
Subscription status is a weak loyalty signal: subscribed customers average only ~1 more previous purchase than non-subscribed customers.
Purchase history beats demographics: high-value customers (top 20% by a composite value score) are best identified by order value and previous purchase count — not age, gender, location, or subscription status.
Satisfaction is broadly uniform: review ratings stay in a tight 3.71–3.79 band across categories and purchase frequency bands, so satisfaction alone doesn't explain repeat-purchase behavior.


- How to Reproduce
Run python/data_preparation.py (or the Colab notebook python/data_preparation_colab.ipynb) to clean the raw dataset.
Run sql/build_database.py to load the cleaned data into a SQLite database.
Run the queries in sql/analysis_queries.sql against sql/retail.db.
Open powerbi/retail_dashboard.pbix in Power BI Desktop to explore the dashboard, or follow powerbi/POWER_BI_GUIDE.md to rebuild it from scratch.
