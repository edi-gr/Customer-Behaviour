# Customer Shopping Behavior & Insights Analysis

## 📌 Project Overview
This project delivers an end-to-end data analytics solution designed to decode customer purchasing patterns for a retail environment. Using a dataset of **3,900 transactions**, I developed a full data pipeline—transitioning from raw data ingestion and cleaning in **Python**, to structured business logic implementation in **SQL**, and final executive-level visualization in **Power BI**.

The goal is to provide actionable intelligence on customer segmentation, subscription value, and the impact of discounts on total revenue.

---

## 🛠️ Technical Stack
* **Data Processing:** Python (Pandas, NumPy)
* **Database Management:** SQL (PostgreSQL/MySQL)
* **Database Connectivity:** SQLAlchemy / Psycopg2
* **Business Intelligence:** Power BI

---

## 📊 Dataset Summary
The analysis is based on 3,900 customer records with 18 key features:
* **Demographics:** Age, Gender, Location.
* **Purchase Details:** Item Category, Purchase Amount ($), Season, Size, Color.
* **Behavioral Metrics:** Previous Purchases, Subscription Status, Frequency, Review Ratings.
* **Logistics:** Shipping Type, Discount Usage, Promo Codes.

---

## 🔄 Project Workflow

### 1. Data Cleaning & Engineering (Python)
I utilized Python to handle the initial "messy" data and prepare it for relational database storage:
* **Missing Value Imputation:** Identified 37 null values in `Review Rating` and imputed them using the **median rating** specific to each product category to maintain data integrity.
* **Feature Engineering:** * Binned customer ages into categorical `Age Groups`.
    * Created a `purchase_frequency_days` metric to quantify customer engagement.
* **Schema Standardization:** Converted all column headers to `snake_case` for seamless SQL integration.
* **Automation:** Developed a script to establish a connection to a SQL Server and automate the data loading process.

### 2. Structured Analysis (SQL)
With the data hosted in a relational database, I executed complex queries to answer high-value business questions:
* **Revenue Analysis:** Calculated total revenue split by gender and subscription status.
* **Customer Segmentation:** Classified users into **New, Returning, and Loyal** segments based on historical purchase frequency.
* **Discount Effectiveness:** Identified "