# Customer Shopping Behavior Analysis
## 1. Project Overview

This project demonstrates an end-to-end data analytics workflow, from data collection and preparation to visualization and reporting. The objective is to extract meaningful insights from a dataset using Python, SQL, and Power BI, then communicate findings through a professional report and presentation.

Key activities include:

* Loading and exploring the dataset in Python
* Performing Exploratory Data Analysis (EDA)
* Cleaning and transforming data
* Running SQL queries for business insights
* Building an interactive Power BI dashboard
* Creating an analytical report

---

## 2. Dataset Summary

**Dataset Name:** customer_behavior.xlsx

**Description:**
The dataset contains customer transaction data from an e-commerce platform, including:
- Customer demographics (gender, subscription status)
- Purchase behavior (amount, category, discount usage)
- Shipping preferences (Standard, Express, Free Shipping)
- Customer feedback (review ratings)

**Key Columns:**
| Column | Description |
| :--- | :--- |
| `customer_id` | Unique customer identifier |
| `gender` | Male / Female |
| `subscription_status` | Yes / No |
| `category` | Accessories / Clothing / Footwear / Outerwear |
| `purchase_amount` | Transaction value in USD |
| `discount_applied` | Yes / No |
| `shipping_type` | Standard / Express / Free Shipping / Store Pickup |
| `review_rating` | 1-5 scale |

---

## Tools & Technologies

| Tool                            | Purpose                             |
| ------------------------------- | ----------------------------------- |
| Python                          | Data loading, cleaning, and EDA     |
| Pandas                          | Data manipulation                   |
| NumPy                           | Numerical operations                |
| PostgreSQL / MySQL / SQL Server | Data querying and analysis          |
| Power BI                        | Dashboard creation                  |
| Microsoft Excel                 | Data validation and rev             |
| Git & GitHub                    | Version control and project sharing |

---

## Project Workflow

### 1. Data Loading

* Imported dataset into Python
* Checked data types and structure
* Identified missing values and duplicates

### 2. Data Cleaning

* Handled missing values
* Removed duplicate records
* Corrected inconsistent data formats
* Standardized column names and values

### 3. SQL Analysis

Executed SQL queries to:

* Calculate KPIs
* Aggregate business metrics
* Identify top-performing categories
* Analyze trends and customer behavior

Example:

```sql
SELECT category,
       SUM(sales) AS total_sales
FROM sales_data
GROUP BY category
ORDER BY total_sales DESC;
```

### 5. Power BI Dashboard

Developed an interactive dashboard featuring:

* KPI cards
* Trend analysis
* Category performance
* Regional analysis
* Filters and slicers for user interaction

---

## Dashboard

### Main Features

* Executive Summary View
* Sales & Performance Analysis
* Customer Insights
* Trend Monitoring
* Interactive Filtering

**Dashboard Preview:**

> <img width="1315" height="720" alt="image" src="https://github.com/user-attachments/assets/c7558b83-4589-4e9e-9796-809dba5716cc" />


---

## Results & Insights
### 1. The Discount Paradox: Subscribers are overusing promotions

> **📊 Finding:** 
> - Only **27%** of customers are Subscribers, yet they account for **62%** of all discount usage.
> - Non-subscribers (73% of the base) use only **37%** of discounts but have nearly identical average order values (**$58 vs $59**).

| SQL Query | Power BI Dashboard |
|:---:|:---:|
| ![Discount SQL](https://github.com/user-attachments/assets/52a9a8bc-563d-4f38-9f83-c25b67d951ef) | ![Discount Dashboard](https://github.com/user-attachments/assets/6248a55a-12f4-43ec-a210-75ff4256d225) |

> **⚠️ Problem:** 
> Discounts are heavily favoring Subscribers, but they aren't driving higher spending. This is essentially "burning" profit margins on our most loyal customers without generating extra revenue.

> **🚀 Recommendation:** 
> Shift Subscriber incentives from **Discounts** to **Loyalty Points**. This maintains retention while protecting profit margins. Launch a "Free Shipping" campaign specifically targeting the **73% Non-subscribers** to convert them into members.

### 2. Gender x Category: "Male Dominates Accessories"

### 2. Gender x Category: "Male Dominates Accessories"

> **🔥 Key Finding:** Contrary to the belief that accessories are "for women," **Male customers dominate** with 69% of customers and 71% of revenue.

| Metric | Male + Accessories | Female + Accessories |
| :--- | :--- | :--- |
| Customers | 848 (69%) | 390 (31%) |
| Total Revenue | ~$50K (71%) | ~$20K (29%) |
| Avg Revenue / Order | $59.41 | $60.76 |
| Total Sales | 800 (67%) | 400 (33%) |

**Power BI Visualizations:**

**Male + Accessories:**
![Male Accessories](https://github.com/user-attachments/assets/37a8ed50-f24c-4e56-8035-3385d45b0768)

**Female + Accessories:**
![Female Accessories](https://github.com/user-attachments/assets/b686f828-160d-43e3-abe1-fb2b98026135)

> **🚀 Action:**
> - **For Male (Core):** Expand men's product lines (watches, belts, wallets) and focus on retention.
> - **For Female (Upsell):** Leverage their higher AOV ($60.76) by creating bundle deals to increase order value.

