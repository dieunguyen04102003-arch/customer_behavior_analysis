# Customer Shopping Behavior Analysis
## I. Project Overview

This project demonstrates an end-to-end data analytics workflow, from data collection and preparation to visualization and reporting. The objective is to extract meaningful insights from a dataset using Python, SQL, and Power BI, then communicate findings through a professional report and presentation.

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
SELECT category, SUM(purchase_amount) AS total_revenue 
FROM customer_behavior 
GROUP BY category 
ORDER BY total_revenue DESC;
```

### 5. Power BI Dashboard

Developed an interactive dashboard featuring:

* KPI cards
* Trend analysis
* Category performance
* Regional analysis
* Filters and slicers for user interaction

---

## V. Dashboard

### Main Features

* Executive Summary View
* Sales & Performance Analysis
* Customer Insights
* Trend Monitoring
* Interactive Filtering

**Dashboard Preview:**

> <img width="1315" height="720" alt="image" src="https://github.com/user-attachments/assets/c7558b83-4589-4e9e-9796-809dba5716cc" />


---

## VI. Results & Insights
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
![Female Accessories](https://github.com/user-attachments/assets/cdf7f496-cffc-4aa0-84f8-2f6d892e6470)

### 🚀 Action & SDLC Alignment

1. **Feature Implementation (Growth & Retention):**
   - **For Male (Core):** Recommend the product team to prioritize expanding men's product lines (watches, belts, wallets) on the UI and personalize recommendations.
   - **For Female (Upsell):** Implement an automated bundle-deal feature at checkout to leverage their higher AOV ($60.76).

2. **Testing Experiment Design (The Discount Paradox):**
   - **A/B Testing Proposal:** Design an experiment to phase out direct discounts for a test group of Subscribers, replacing them with a Loyalty Points system to evaluate margin recovery without affecting retention.
   - **Growth Campaign:** Design and launch a targeted "Free Shipping" campaign UI component tailored specifically for the 73% Non-subscribers to test conversion rate uplifts into full subscriptions.
### 3. Product Funnel Optimization Concept (User Journey)
To align this transactional data with standard Product Analytics Frameworks, we map out the simulated E-commerce funnel below to identify drop-off points:

* **Funnel Stages:** `View Product` ➔ `Add to Cart` ➔ `Purchase (Non-Subscribed)` ➔ `Upgrade to Subscription`
* **The Subscription Drop-off:** While **73%** of our total active users complete purchases as Non-subscribers, only **27%** convert into Subscribers. 
* **Product Insight:** Non-subscribers maintain a high Average Order Value (AOV) of **$58**. The friction isn't the price or intent to buy—it's the friction in the subscription onboarding flow.
* **Growth Action:** Implement a targeted "1-Click Subscription Upgrade" at the checkout success page for Non-subscribers to bridge this gap.

### 4. Proposed Automated Data Alerts (Product Health Monitoring)
To help the Product & Data teams catch anomalies early and monitor product health daily, we propose setting up the following automated data triggers:

| Alert Trigger | Threshold | Business Reason |
| :--- | :--- | :--- |
| **🚨 Subscriber Discount Exploitation** | Over **65%** | Alerts Product Team when promos are burning too much margin on existing loyalists without driving extra basket size. |
| **📉 Category Rating Drop** | Below **3.5 / 5.0** | Signals potential quality issues, delivery friction, or bugs in specific product pages (e.g., Clothing, Accessories). |
| **⚠️ High Outlier Order Value** | 3x above average | Detects bulk-buying anomalies, wholesaling behavior, or system payment glitches. |

---

## VII. Conclusion & Future Outlook

### 🎯 Project Conclusion
This project successfully transitions raw transaction logs into high-value business insights. By discovering the **Discount Paradox** (loyal users consuming margins without increasing order size) and the **Male-dominated Accessories segment**, the analysis provides the Product and Marketing teams with clear, data-backed strategies to optimize revenue and membership conversion.

### 🔮 Future Outlook (Next Steps)
If given more data and time, the project will be expanded with:
1. **Predictive Churn Modeling:** Using Python (`scikit-learn`) to build a machine learning model that predicts which subscribers are likely to cancel their membership based on their purchase frequency.
2. **RFM Customer Segmentation:** Implementing Advanced RFM (Recency, Frequency, Monetary) clustering to divide the user base into distinct micro-segments for personalized email marketing automation.
3. **Live Data Pipeline:** Migrating the local `.csv` file into a cloud database (e.g., AWS S3 or Google BigQuery) and scheduling automatic daily dashboard refreshes.
