# Customer Shopping Behavior Analysis
## I. Business Problem

> An e-commerce company wants to understand customer purchasing behavior and evaluate whether its current promotional strategy is effective.

> This project analyzes customer transaction data to answer the following business questions:

> - Which customer segments contribute the most revenue?
> - Are discount campaigns increasing customer spending?
> - Which product categories perform best?
> - What actions can improve marketing efficiency and customer retention?

Key activities include:

* Loading and exploring the dataset in Python
* Performing Exploratory Data Analysis (EDA)
* Cleaning and transforming data
* Running SQL queries for business insights
* Building an interactive Power BI dashboard
* Creating an analytical report

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
| PostgreSQL / MySQL / SQL Server | Data querying and analysis          |
| Power BI                        | Dashboard creation                  |
| Microsoft Excel                 | Data validation and rev             |
| Git & GitHub                    | Version control and project sharing |

---

## IV. Project Workflow

Business Questions
      ↓
Data Understanding
      ↓
Data Cleaning
      ↓
Exploratory Data Analysis
      ↓
SQL Analysis
      ↓
Dashboard
      ↓
Business Insights
      ↓
Recommendations

### 1. Data Cleaning

The dataset was prepared before analysis by:

* Checking missing values
* Removing duplicate records
* Standardizing categorical values
* Verifying data types
* Validating data consistency

### 2. SQL Analysis

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

### 3. Power BI Dashboard

The dashboard provides interactive visualizations for:

> - Revenue overview
> - Customer segmentation
> - Product category performance
> - Discount analysis
> - Key business KPIs

**Dashboard Preview:**

> <img width="1315" height="720" alt="image" src="https://github.com/user-attachments/assets/c7558b83-4589-4e9e-9796-809dba5716cc" />


---

## V. Key Findings
### 1. Discount Campaigns Show Limited Impact on Customer Spending

> **Business Question:**
> Are discount campaigns increasing customer spending?

> **Finding:** 
> - Subscribers represent 27% of customers but receive 62% of all discounts.
> - Their Average Order Value is almost the same as non-subscribers.

| SQL Query | Power BI Dashboard |
|:---:|:---:|
| ![Discount SQL](https://github.com/user-attachments/assets/52a9a8bc-563d-4f38-9f83-c25b67d951ef) | ![Discount Dashboard](https://github.com/user-attachments/assets/6248a55a-12f4-43ec-a210-75ff4256d225) |

> **Business Impact:**
> The company may be spending more on promotions without generating additional revenue.

> **Recommendation:**
> Consider replacing broad discount campaigns with a loyalty points program to attract non-subscribers.


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


## VI. Business Recommendations

> Based on the findings, the company could consider:

> - Optimizing discount allocation to improve promotion efficiency.
> - Introducing a loyalty program to encourage repeat purchases.
> - Personalizing marketing campaigns based on customer purchasing behavior.
> - Monitoring promotion performance using key business KPIs.


## VII. Conclusion
> This project demonstrates a complete data analysis workflow using Python, SQL, and Power BI to transform raw transaction data into business insights.

> The findings highlight opportunities to improve promotional strategies, better understand customer purchasing behavior, and support data-driven decision-making.
