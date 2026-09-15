# Customer Behavior Analytics Project

## Overview

This project demonstrates an end-to-end **Data Analyst workflow**, starting from raw customer and purchase data and ending with business insights presented through SQL analysis, a Power BI dashboard, a written report, and a presentation.

The project focuses on understanding customer purchasing behaviour, product performance, revenue patterns, and customer demographics.

The workflow includes:

**Data Loading → Exploratory Data Analysis → Data Cleaning → SQL Analysis → Power BI Dashboard → Business Report → Presentation**

---

## Project Objectives

The main objectives of this project are to:

* Understand customer purchasing behaviour
* Analyse revenue and purchase patterns
* Identify top-performing products and categories
* Analyse customer demographics
* Perform data quality checks and cleaning
* Use SQL to answer business questions
* Build an interactive Power BI dashboard
* Communicate findings through a report and presentation

---

## Dataset

The project uses a customer purchase dataset containing information such as:

* Customer ID
* Age
* Gender
* Category
* Item Purchased
* Purchase Amount
* Review Rating
* Location
* Subscription Status
* Payment Method
* Shipping Type
* Previous Purchases
* Frequency of Purchases
* Other customer and purchase attributes

The dataset was initially loaded and explored using Python before being stored in PostgreSQL for SQL-based analysis.

---

## Tools & Technologies

| Tool           | Purpose                                   |
| -------------- | ----------------------------------------- |
| **Python**     | Data loading, exploration and preparation |
| **Pandas**     | Data manipulation and cleaning            |
| **NumPy**      | Data analysis and calculations            |
| **Matplotlib** | Exploratory data visualisation            |
| **PostgreSQL** | Database storage and SQL analysis         |
| **pgAdmin**    | PostgreSQL database management            |
| **SQL**        | Business analysis and data querying       |
| **Power BI**   | Dashboard and interactive visualisation   |
| **PowerPoint** | Business presentation                     |
| **Git/GitHub** | Version control and project documentation |

---

## Project Workflow

### 1. Load Data into Python

The dataset was loaded into Python using Pandas.

The initial analysis included:

* Inspecting the dataset structure
* Checking rows and columns
* Understanding data types
* Reviewing unique values
* Identifying missing values
* Identifying duplicate records
* Understanding numerical and categorical variables

Example:

```python
import pandas as pd

df = pd.read_csv("customer_data.csv")

print(df.head())
print(df.shape)
print(df.info())
print(df.isnull().sum())
```

---

### 2. Exploratory Data Analysis (EDA)

EDA was performed to understand the characteristics and patterns in the dataset.

The analysis included:

* Customer demographics
* Purchase amount distribution
* Product and category performance
* Review ratings
* Purchase frequency
* Subscription behaviour
* Payment methods
* Customer purchasing patterns

Visualisations were created using Python to identify trends, distributions and potential data-quality issues.

---

### 3. Data Cleaning

The dataset was cleaned before performing the final analysis.

Key activities included:

* Handling missing values
* Removing duplicate records
* Correcting inconsistent values
* Standardising categorical data
* Converting columns to appropriate data types
* Checking numerical values for inconsistencies
* Validating the cleaned dataset

The cleaned dataset was then prepared for database analysis.

---

### 4. Load Data into PostgreSQL

The cleaned dataset was loaded into a PostgreSQL database.

The database was accessed and managed using **pgAdmin**.

PostgreSQL was used to perform structured SQL analysis and answer business questions.

---

### 5. SQL Analysis

SQL queries were developed to answer business-related questions.

Examples include:

* What is the total revenue?
* What is the revenue by gender?
* Which products have the highest average review rating?
* What are the top 3 most purchased products within each category?
* Which categories generate the most revenue?
* What are the most common payment methods?
* How does subscription status affect purchasing behaviour?
* Which customer groups have the highest purchase activity?

SQL techniques used include:

* `SELECT`
* `WHERE`
* `GROUP BY`
* `HAVING`
* `ORDER BY`
* Aggregate functions
* `CASE WHEN`
* Common Table Expressions (CTEs)
* Window functions
* `ROW_NUMBER()`
* `DENSE_RANK()`
* Subqueries

Example:

```sql
SELECT 
    category,
    SUM("Purchase_Amount") AS revenue
FROM public."Customer"
GROUP BY category
ORDER BY revenue DESC;
```

---

## Power BI Dashboard

The cleaned and analysed data was used to create an interactive Power BI dashboard.

### Dashboard Features

The dashboard provides insights into:

* Total revenue
* Total purchases
* Average purchase amount
* Average review rating
* Revenue by category
* Revenue by gender
* Top-performing products
* Customer purchasing behaviour
* Subscription analysis
* Payment method distribution

### Power BI Techniques

The dashboard includes:

* Data modelling
* Relationships
* DAX measures
* KPI cards
* Bar charts
* Column charts
* Donut charts
* Slicers
* Interactive filtering
* Drill-down where appropriate

The dashboard is designed to allow users to explore customer and sales performance interactively.

---

## Business Report

A separate business report was created to document the analysis and findings.

The report covers:

1. Business objectives
2. Dataset description
3. Data preparation
4. Exploratory analysis
5. SQL analysis
6. Power BI dashboard
7. Key findings
8. Business recommendations

The report focuses on translating technical analysis into clear business insights.

---

## Presentation

A PowerPoint presentation was created to communicate the project to a non-technical audience.

The presentation includes:

* Business problem
* Data and methodology
* Key analysis
* Important findings
* Power BI dashboard
* Business recommendations
* Conclusion

The presentation is designed to demonstrate the ability to communicate data insights clearly to stakeholders.

---

## Key Results

The analysis provides insights into:

* Products and categories contributing the most revenue
* Products with strong customer ratings
* Customer purchasing patterns
* Differences in purchasing behaviour across customer segments
* Popular payment methods
* Subscription and purchasing behaviour
* Top-performing products within each category

These findings can help businesses better understand customers, identify high-performing products and support data-driven decision-making.

---

## Project Structure

```text
Customer-Purchase-Analytics/
│
├── data/
│   └── customer_data.csv
│
├── python/
│   ├── data_loading.ipynb
│   ├── eda.ipynb
│   └── data_cleaning.ipynb
│
├── sql/
│   └── customer_analysis.sql
│
├── powerbi/
│   └── customer_purchase_dashboard.pbix
│
├── report/
│   └── customer_purchase_analysis.pdf
│
├── presentation/
│   └── customer_purchase_analysis.pptx
│
├── screenshots/
│   └── dashboard.png
│
└── README.md
```

---

## How to Run the Project

### Step 1 – Clone the Repository

```bash
git clone <repository-url>
cd Customer-Purchase-Analytics
```

### Step 2 – Set Up Python

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib jupyter
```

Run the notebooks in the following order:

```text
1. data_loading.ipynb
2. eda.ipynb
3. data_cleaning.ipynb
```

### Step 3 – Set Up PostgreSQL

1. Install PostgreSQL and pgAdmin.
2. Create a database.
3. Create/import the `Customer` table.
4. Load the cleaned dataset.
5. Run the SQL queries from:

```text
sql/customer_analysis.sql
```

### Step 4 – Open Power BI

Open the Power BI file:

```text
powerbi/customer_purchase_dashboard.pbix
```

Update the data source connection if required and refresh the dataset.

---

## Skills Demonstrated

This project demonstrates practical experience in:

**Data Analysis**

* Exploratory Data Analysis
* Data Cleaning
* Data Validation
* Business Analysis

**SQL**

* Aggregations
* Joins
* CTEs
* Subqueries
* Window Functions
* Ranking
* Business-focused SQL analysis

**Power BI**

* Data Modelling
* DAX
* Interactive Dashboards
* KPI Development
* Data Visualisation

**Python**

* Pandas
* NumPy
* Matplotlib
* Data Preparation
* EDA

**Business Communication**

* Data storytelling
* Business reporting
* Presentation of insights
* Recommendations

---

## Conclusion

This project demonstrates an end-to-end approach to solving a business problem using data.

It combines **Python, SQL, PostgreSQL and Power BI** to transform raw customer data into meaningful business insights, supported by a professional report and presentation.

The project highlights both technical data analysis skills and the ability to communicate analytical results to business stakeholders.
