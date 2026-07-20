# Customer Shopping Behavior Analysis
## I. Business Problem

An e-commerce company wants to understand customer purchasing behavior and evaluate whether its current promotional strategy is effective.

This project analyzes customer transaction data to answer the following business questions:

Which customer segments contribute the most revenue?
Are discount campaigns increasing customer spending?
Which product categories perform best?
What actions can improve marketing efficiency and customer retention?

Key activities include:

* Loading and exploring the dataset in Python
* Performing Exploratory Data Analysis (EDA)
* Cleaning and transforming data
* Running SQL queries for business insights
* Building an interactive Power BI dashboard
* Creating an analytical report

Mapping transactional data into Product Analytics Frameworks to identify user journey drop-offs. 

Aligning data insights with the Software Development Life Cycle (SDLC) to drive feature prioritization and testing experiments.

## II. Dataset Summary

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

## III. Tools & Technologies

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

## IV. Project Workflow

### 1. Data Loading

* Imported dataset into Python
* Checked data types and structure

### 2. Data Cleaning

The dataset was prepared before analysis by:

* Checking missing values
* Removing duplicate records
* Standardizing categorical values
* Verifying data types
* Validating data consistency

### 3. SQL Analysis

SQL was used to answer business questions such as:

* Revenue by product category
* Customer segmentation
* Discount utilization
* Average order value
* Subscription performance

Example:

```sql
SELECT category, SUM(purchase_amount) AS total_revenue 
FROM customer_behavior 
GROUP BY category 
ORDER BY total_revenue DESC;
```

### 5. Power BI Dashboard

The Power BI dashboard provides an overview of:

* Executive KPI Summary
* Revenue Analysis
* Customer Segmentation
* Discount Performance
* Product Category Performance

**Dashboard Preview:**

> <img width="1315" height="720" alt="image" src="https://github.com/user-attachments/assets/c7558b83-4589-4e9e-9796-809dba5716cc" />


---

## V. Key Findings
### 1. Discount Strategy Is Not Driving Higher Spending

> **Business Question:**
> Are discount campaigns increasing customer spending?

> **Finding:** 
> - Subscribers represent 27% of customers but receive 62% of all discounts.
> - Their Average Order Value is almost the same as non-subscribers.

| SQL Query | Power BI Dashboard |
|:---:|:---:|
| ![Discount SQL](https://github.com/user-attachments/assets/52a9a8bc-563d-4f38-9f83-c25b67d951ef) | ![Discount Dashboard](https://github.com/user-attachments/assets/6248a55a-12f4-43ec-a210-75ff4256d225) |

> **Business Impact:**
> The current promotion strategy may reduce profit margins without encouraging customers to spend more.

> **Recommendation:**
> Consider replacing broad discount campaigns with a loyalty points program while using targeted promotions to attract non-subscribers.


### 2. Accessories Generate Strong Revenue from Male Customers

> **Business Question:**
>Which customer segment contributes the most revenue?

> **Finding:**
> - Male customers account for 71% of accessory revenue.
> - Female customers have a slightly higher average order value.

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
![Female Accessories](https://github.com/user-attachments/assets/cdf7f496-cffc-4aa0-84f8-2f6d892e6470)

> **Business Impact:**
> Different customer groups show different purchasing patterns, suggesting opportunities for more personalized marketing strategies.

> **Recommendation:**
> Focus product recommendations for male customers while testing bundle promotions for female customers to increase basket size.


---

## VI. Business Recommendations**

> Based on the analysis, the following actions are recommended:

> - Optimize discount allocation instead of applying promotions broadly.
> - Develop a loyalty program to improve long-term customer retention.
> - Personalize marketing campaigns based on customer purchasing behavior.
> - Monitor promotion performance using key business KPIs.
