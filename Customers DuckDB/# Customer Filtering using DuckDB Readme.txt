# Customer Filtering using DuckDB and Python

## Overview
This project performs customer purchase analysis using **DuckDB** and **Python**.  
It uses two datasets:
1. **customers.csv** — Contains customer details (`id`, `name`, `age`, `email`)
2. **purchases.csv** — Contains purchase records (`customer_id`, `product_id`, `quantity`)

The objective is to join, group, filter, and analyze customer data using SQL queries in DuckDB.

---

## Tasks Performed

### 1. Join and Group Data
- Joined `customers` and `purchases` on `customer_id`.
- Grouped by customer ID, name, and age.
- Calculated the **total quantity purchased** by each customer.

**Insight:**  
Shows total items purchased per customer.

---

### 2. Filter by Quantity and Age
- Filtered customers who:
  - Purchased **more than 5 items**.
  - Are **younger than 30**.

**Insight:**  
Identifies young, high‑volume buyers for targeted campaigns.

---

### 3. Identify Customers with Multiple Product Categories
- Counted distinct products per customer.
- Selected customers with **two or more distinct products**.

**Insight:**  
Highlights customers with diverse buying behavior.

---

### 4. Calculate Total Spending for Customers Aged 30+
- Selected customers aged **30+**.
- Summed total quantity purchased.

**Insight:**  
Provides an overview of older customers’ purchasing contributions.

---

## Tools Used
- **Python 3** — Main programming language
- **Pandas** — Data handling and preprocessing
- **DuckDB** — SQL execution on in‑memory DataFrames

---

## How to Run
1. Install dependencies in Google Colab:
   ```bash
   pip install duckdb pandas
