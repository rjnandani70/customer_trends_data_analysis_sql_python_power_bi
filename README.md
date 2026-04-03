# 👨🏻‍💻 Customer Behavior Data Analyst Portfolio Project

This project represents a complete, industry-standard, end-to-end data analytics workflow, designed to mirror the real responsibilities of professional analysts in modern business environments. The project encompasses all critical stages of data analysis, from data preparation and modeling to insight generation, visualization, and reporting.

---

## 📌 Project Overview

The goal of this project is to simulate a corporate-grade end-to-end data analytics workflow, demonstrating the ability to translate raw data into strategic business intelligence by:

- **Data Preparation, Modeling & Exploratory Data Analysis (Python):** Clean and transform the raw dataset for analysis.

- **Data Analysis (SQL):** Simulate business transactions, and run queries to extract insights on customer segments, loyalty, and purchase drivers.

- **Visualization & Insights (Power BI):** Build an interactive dashboard that highlights key patterns and trends, enabling stakeholders to make data-driven decisions.

- **Report and Presentation:** Write a clear project report summarizing your key findings and business recommendations. Prepare a presentation that visually communicates insights and actionable recommendations to stakeholders.

---

## 🛠️ Tools Used in the Project

1. **Python**
   - Libraries: `pandas`, `sqlalchemy`
   - PostgreSQL connector: `pg8000`

2. **PostgreSQL Database**
   - Database Name: `customer_behavior`
   - Host: `localhost`
   - Port: `5432`

3. **Power BI**
   - Used to load data from PostgreSQL and create visualizations.

---

## 🛠️ How to Use This Project

### **1. Set Up the Environment**

1. Install required tools:
   - **Python (Anaconda or standalone Python)**
   - **PostgreSQL + pgAdmin**
   - **VS Code / Jupyter Notebook**
   - **Power BI Desktop**
2. Download project files:
   - `Customer_Shopping_Behavior_Analysis.ipynb`
   - `customer_behavior_sql_queries.sql`
   - `customer_behavior_powerBI_dashboard.pbix`
   - Dataset: `customer_shopping_data.csv`

### **2. Python: Exploratory Data Analysis & Data Loading**

#### **Step 2.1: Open the Notebook**

Open `Customer_Shopping_Behavior_Analysis.ipynb` to:

- Import the dataset
- Perform data exploration
- Clean the data
- Load data into PostgreSQL

#### **Step 2.2: Import Required Python Libraries**

```python
import pandas as pd
from sqlalchemy import create_engine
```

#### **Step 2.3: Load & Explore Dataset**

- Load CSV
- Check missing values
- Understand distributions

Example:

```python
df = pd.read_csv("customer_shopping_data.csv")
df.head()
df.info()
df.describe()
```

#### **Step 2.4: Clean the Data**

- Handle missing values
- Remove duplicates
- Convert data types
- Standardize column names

#### **Step 2.5: Connect Python to PostgreSQL**

Create a database in PostgreSQL, for example:

```sql
CREATE DATABASE customer_behavior_db;
```

Then connect:

```python
engine = create_engine("postgresql://username:password@localhost:5432/customer_behavior_db")
```

#### **Step 2.6: Load Data from Python → PostgreSQL Table**

```python
df.to_sql("customer_behavior", engine, index=False, if_exists="replace")
```

---

### **3. SQL Analysis Using PostgreSQL**

#### **Step 3.1: Open the SQL File**

Open `customer_behavior_sql_queries.sql` to:

- Analyze customer segmentation
- Identify purchase trends
- Extract insights on shipping types, discounts, and high-value customers

#### **Step 3.2: Connect to Your Database in pgAdmin**

- Database: `customer_behavior_db`
- Table: `customer_behavior`

#### **Step 3.3: Run All Business Questions**

Examples:

- Compare purchase amounts by shipping type
- Find customers with the highest lifetime value
- Identify products with the highest discount usage
- Analyze sales trends by month

---

### **4. Connect PostgreSQL Data to Power BI**

#### **Step 4.1: Open Power BI Desktop**

- File: `customer_behavior_powerBI_dashboard.pbix`

#### **Step 4.2: Connect to PostgreSQL**

1. Click **Get Data**
2. Choose **PostgreSQL Database**
3. Enter server and DB name:
   - Server: `localhost`
   - Database: `customer_behavior_db`
4. Load the relevant table: `customer_behavior`

#### **Step 4.3: Clean & Model Data (Power Query Editor)**

- Check column data types
- Remove nulls
- Rename fields
- Create date hierarchy

#### **Step 4.4: Create Visualizations**

- **Sales by Product Category** – Bar chart
- **Monthly Sales Trend** – Line chart
- **Top Customers by Spending** – Horizontal bar
- **Shipping Type Distribution** – Donut/Pie
- **Discount Impact on Revenue** – Column chart
- **Filters/Slicers**: month, product, gender, age segment

#### **Step 4.5: Build Interactive Dashboard**

Include:

- Key Metrics (cards):
  - Total Revenue
  - Total Orders
  - Avg Purchase Amount
  - Discounted vs Non-discounted Sales
- Charts + Filters
- Navigation panels (optional)

---

### ✅ **Methodology**

Python → SQL → Power BI pipeline.

### ✅ **Insights**

- Customer purchase behavior
- Shipping trends
- Discount analysis
- Category performance
- High-value customers

### ✅ **Recommendations**

Insights-based suggestions for business improvement.

---

© 2026 Raj Nandani. All rights reserved.