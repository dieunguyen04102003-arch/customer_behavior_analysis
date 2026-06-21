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

**Dataset Name:** *[Insert Dataset Name]*

**Source:** *[Insert Source or Link]*

**Description:**
The dataset contains information related to *[business domain, e.g., sales, customers, finance, healthcare, etc.]* and is used to identify trends, patterns, and key performance indicators (KPIs).

**Key Columns:**

* `Column 1`
* `Column 2`
* `Column 3`
* `Column 4`

---

## Tools & Technologies

| Tool                            | Purpose                             |
| ------------------------------- | ----------------------------------- |
| Python                          | Data loading, cleaning, and EDA     |
| Pandas                          | Data manipulation                   |
| NumPy                           | Numerical operations                |
| Matplotlib / Seaborn            | Data visualization                  |
| PostgreSQL / MySQL / SQL Server | Data querying and analysis          |
| Power BI                        | Dashboard creation                  |
| Microsoft Excel                 | Data validation and review          |
| Gamma                           | Presentation creation               |
| Git & GitHub                    | Version control and project sharing |

---

## Project Workflow

### 1. Data Loading

* Imported dataset into Python
* Checked data types and structure
* Identified missing values and duplicates

### 2. Exploratory Data Analysis (EDA)

* Generated summary statistics
* Analyzed distributions and trends
* Created visualizations to identify patterns
* Explored relationships between variables

### 3. Data Cleaning

* Handled missing values
* Removed duplicate records
* Corrected inconsistent data formats
* Standardized column names and values

### 4. SQL Analysis

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

> Add screenshots of your Power BI dashboard here.

---

## Results & Insights
### 1. The Discount Paradox: Subscribers are overusing promotions

> **📊 Finding:** 
> - Only **27%** of customers are Subscribers, yet they account for **62%** of all discount usage.
> - Non-subscribers (73% of the base) use only **37%** of discounts but have nearly identical average order values (**$58 vs $59**).

<div style="display: flex; gap: 10px;">
  <img width="654" height="366" alt="image" src="https://github.com/user-attachments/assets/52a9a8bc-563d-4f38-9f83-c25b67d951ef" width="48%"/>
  <img width="368" height="266" alt="image" src="https://github.com/user-attachments/assets/6248a55a-12f4-43ec-a210-75ff4256d225" width="48%" />
</div>

> **⚠️ Problem:** 
> Discounts are heavily favoring Subscribers, but they aren't driving higher spending. This is essentially "burning" profit margins on our most loyal customers without generating extra revenue.

> **🚀 Recommendation:** 
> Shift Subscriber incentives from **Discounts** to **Loyalty Points**. This maintains retention while protecting profit margins. Launch a "Free Shipping" campaign specifically targeting the **73% Non-subscribers** to convert them into members.





### Business Impact

* Improved understanding of key metrics.
* Enabled data-driven decisions.
* Simplified reporting through visualization.

---

## Deliverables

* Python Analysis Notebook (`.ipynb`)
* SQL Scripts (`.sql`)
* Power BI Dashboard (`.pbix`)
* Analytical Report (`.pdf`)
* Gamma Presentation (`.pptx` or share link)

---

## Project Structure

```text
Data-Analytics-Project/
│
├── data/
│   └── dataset.csv
│
├── notebooks/
│   └── analysis.ipynb
│
├── sql/
│   └── queries.sql
│
├── dashboard/
│   └── dashboard.pbix
│
├── reports/
│   └── report.pdf
│
├── presentation/
│   └── gamma_presentation.pptx
│
└── README.md
```

---

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/project-name.git
cd project-name
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Analysis

```bash
jupyter notebook
```

Open the notebook in the `notebooks/` folder and execute all cells.

### 4. Run SQL Queries

Connect to your database and execute the scripts inside the `sql/` folder.

### 5. Open Dashboard

Launch the `.pbix` file using Power BI Desktop.

---

## Author

**Your Name**
Data Analyst | SQL | Python | Power BI

LinkedIn: *[Your LinkedIn Profile]*
Portfolio: *[Your Portfolio Link]*

---

⭐ If you found this project useful, consider giving it a star on GitHub.
