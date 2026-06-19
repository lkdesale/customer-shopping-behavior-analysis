# Retail Customer Shopping Behavior & Trends Analysis

An end-to-end Data Analytics project that analyzes retail customer shopping behavior to uncover purchasing trends, customer value drivers, loyalty patterns, and business opportunities. The project demonstrates the complete analytics workflow—from raw data preparation and feature engineering in Python, to relational data modeling and business analysis in SQL, and finally interactive dashboard development in Power BI.

## Business Problem

A retail company wants to better understand customer shopping behavior to improve sales performance, customer satisfaction, retention, and long-term loyalty.

This project answers the following business question:

**"How can consumer shopping data be leveraged to identify trends, improve customer engagement, and optimize marketing and product strategies?"**

---

## Tech Stack

* **Python (Pandas, NumPy)** – Data cleaning, preprocessing, and feature engineering
* **SQL (SQLite)** – Star schema data modeling and business analytics queries
* **Power BI** – Interactive dashboard development and visualization
* **Microsoft Word** – Project documentation and reporting

---

## Project Structure

```text
├── data/                  # Raw and cleaned datasets
├── python/                # Data cleaning & feature engineering scripts
├── sql/                   # Database schema, SQL queries, and SQLite database
├── powerbi/               # Dashboard source tables, PBIX file, and build guide
├── report/                # Final project report
└── README.md
```

---

## Project Workflow

### 1. Data Preparation (Python)

Processed and cleaned a retail shopping dataset containing approximately 3,900 customer records.

Key tasks included:

* Standardized column names and formats
* Handled missing values using category-level median imputation
* Created age-group segmentation features
* Built a composite Customer Value Score
* Identified High-Value Customers using scoring thresholds
* Simulated purchase dates for time-series analysis
* Added Online/Offline sales channel classification

### 2. Data Modeling & Analysis (SQL)

Designed and implemented a star-schema database model:

* `dim_customers`
* `dim_products`
* `fact_transactions`

Developed 14 business-focused SQL analyses covering:

* Customer segmentation
* Revenue performance
* Channel effectiveness
* Loyalty and repeat-purchase behavior
* Product and purchase drivers
* Customer value analysis

### 3. Data Visualization (Power BI)

Created a 4-page interactive dashboard:

#### Overview

* Revenue KPIs
* Sales trends
* Channel performance
* Category performance

#### Customer Segments

* Demographic analysis
* High-value customer identification
* Customer distribution insights

#### Loyalty & Repeat Purchase Drivers

* Subscription analysis
* Repeat purchase behavior
* Customer retention indicators

#### Purchase Drivers

* Discount impact
* Product category performance
* Customer satisfaction metrics

Interactive slicers allow filtering by:

* Season
* Sales Channel
* Product Category

### 4. Reporting

Prepared a comprehensive project report documenting:

* Methodology
* Data preparation process
* Analytical approach
* Dashboard design
* Key findings
* Business recommendations

---

## Key Findings

### Online Channel Dominates Revenue

* Approximately **78% of orders** originate from the Online channel.
* Approximately **78% of total revenue** is generated online.
* Online sales produce roughly **3.6x more revenue** than Offline sales.

### Discounts Have Minimal Impact

* Average order value remains nearly unchanged regardless of discount usage.
* Customer review ratings are also similar between discounted and non-discounted purchases.
* Current discount strategies appear to have limited influence on customer behavior.

### Subscription Status Is a Weak Loyalty Indicator

* Subscribed customers average only about **one additional previous purchase** compared to non-subscribers.
* Subscription alone is not a strong predictor of repeat purchasing.

### Purchase History Outperforms Demographics

High-value customers are better identified through:

* Order value
* Previous purchase count
* Customer Value Score

Demographic variables such as:

* Age
* Gender
* Location
* Subscription status

show relatively weak predictive power.

### Customer Satisfaction Is Consistent Across Segments

* Average review ratings remain within a narrow range of approximately **3.71–3.79**.
* Satisfaction levels are similar across product categories and purchase frequency groups.
* Satisfaction alone does not explain repeat-purchase behavior.

---

## Business Recommendations

* Prioritize investment in Online sales channels.
* Redesign discount strategies and focus on targeted promotions.
* Develop loyalty programs based on purchasing behavior rather than subscription status.
* Use transaction history and customer value metrics for customer segmentation.
* Focus retention efforts on high-value customer groups.
* Explore additional drivers of repeat purchasing beyond customer satisfaction scores.

---

## How to Reproduce

### Step 1: Data Preparation

Run:

```bash
python python/data_preparation.py
```

or use:

```text
python/data_preparation_colab.ipynb
```

### Step 2: Build Database

Run:

```bash
python sql/build_database.py
```

This will generate:

```text
sql/retail.db
```

### Step 3: Execute Analysis Queries

Run the SQL scripts located in:

```text
sql/analysis_queries.sql
```

against:

```text
sql/retail.db
```

### Step 4: Explore Dashboard

Open:

```text
powerbi/retail_dashboard.pbix
```

using Power BI Desktop to interact with the dashboard and explore insights.

---

## Project Outcome

This project demonstrates a complete end-to-end Data Analytics workflow, combining data engineering, SQL analytics, business intelligence, and storytelling to transform raw retail transaction data into actionable business insights and strategic recommendations.
