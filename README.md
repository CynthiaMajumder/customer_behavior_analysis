
# 🛍️ Customer Shopping Behavior — End-to-End Data Analytics Project
---

## 📌 Overview

This is a complete end-to-end data analytics project that analyzes **customer shopping behavior** to uncover trends in revenue, product performance, customer segmentation, and purchasing patterns.

The project covers the full analytics pipeline — from raw data ingestion and cleaning in Python, to SQL-based analysis, and finally to an interactive Power BI dashboard and a presentation built in PPTX.

---

## 📂 Dataset

| Detail | Info |
|--------|------|
| **File** | `customer_shopping_behavior.xlsx` |
| **Records** | ~3,900 rows |
| **Features** | Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount (USD), Location, Size, Color, Season, Review Rating, Subscription Status, Shipping Type, Discount Applied, Promo Code Used, Previous Purchases, Payment Method, Frequency of Purchases |
| **Source** | Kaggle / Provided dataset |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Python (Pandas)** | Data loading, EDA, and cleaning |
| **Jupyter Notebook** | Development environment |
| **MySQL** | Storing data and running SQL queries |
| **MySQL Workbench** | Database management and query execution |
| **SQLAlchemy** | Connecting Python to MySQL |
| **Power BI Desktop** | Interactive dashboard and visualizations |
| **Gamma** | Presentation / PPT creation |

---

## 🔄 Project Steps

### 1️⃣ Data Loading (Python)
- Loaded the Excel dataset using `pandas.read_excel()`
- Connected Jupyter Notebook to the project directory
- Previewed data with `.head()`, `.shape()`, `.info()`

### 2️⃣ Exploratory Data Analysis (EDA)
- Checked dataset shape, column names, and data types
- Identified missing values using `.isnull().sum()`
- Explored distributions of key columns (age, purchase amount, gender, season)
- Analyzed unique values in categorical columns

### 3️⃣ Data Cleaning
- Standardized column names (lowercase + underscores)
- Handled missing/null values
- Removed duplicate rows
- Corrected data types where needed

### 4️⃣ Loading Data into MySQL
- Connected Python to MySQL using `SQLAlchemy` + `mysql-connector-python`
- Pushed cleaned DataFrame to MySQL database using `.to_sql()`
- Verified data load in MySQL Workbench

### 5️⃣ SQL Analysis (MySQL)
Key business questions answered:

| # | Question |
|---|----------|
| Q1 | Total revenue by male vs. female customers |
| Q2 | Customers who used a discount but spent above average |
| Q3 | Top 5 products with highest average review rating |
| Q4 | Revenue by shipping type |
| Q5 | Subscription vs non-subscription customer count & revenue |
| Q6 | Top 5 items by discount conversion rate |
| Q7 | Customer segmentation (New / Returning / Loyal) |

### 6️⃣ Power BI Dashboard
- Connected Power BI to MySQL database
- Built interactive visuals: bar charts, pie charts, KPI cards, slicers
- Added filters for gender, season, category, and subscription status

### 7️⃣ Report & Presentation
- Written report summarizing key findings and business insights
- Presentation created using pptx with clean visuals and recommendations

---

## 📊 Dashboard Highlights

- 💰 **Total Revenue** by Gender, Category, and Season
- ⭐ **Top Rated Products** by average review score
- 🎯 **Customer Segments** — New, Returning, Loyal
- 🚚 **Revenue by Shipping Type**
- 🎟️ **Discount Impact** on purchase behavior

---

## 📈 Key Results & Insights

- Female customers contributed slightly more revenue than male customers overall
- **Clothing** was the top-performing category by revenue
- Customers with **subscriptions** had higher average purchase amounts
- **Free shipping** was the most preferred shipping method
- Loyal customers (10+ previous purchases) made up a significant portion of total revenue
- Discount usage was high but did not always lead to higher spending

---

## 🚀 How to Run This Project

### Prerequisites
Make sure you have the following installed:
- Python 3.x
- Anaconda / Jupyter Notebook
- MySQL 8.0 + MySQL Workbench
- Power BI Desktop
- Required Python libraries:

```bash
pip install pandas openpyxl sqlalchemy mysql-connector-python
```

### Steps

**1. Clone or download this repository**
```bash
git clone https://github.com/yourusername/customer-shopping-analysis.git
```

**2. Open Jupyter Notebook**
```bash
jupyter notebook
```

**3. Run the notebook**

Open `customer_behaviour.ipynb` and run all cells from top to bottom.

**4. Set up MySQL**

Create a database in MySQL Workbench:
```sql
CREATE DATABASE customer_behaviour;
```

**5. Update your connection details in the notebook**
```python
username = "root"
password = "your_password"
host = "127.0.0.1"
port = "3306"
database = "customer_behaviour"
```

**6. Run SQL queries**

Open `customer_analysis.sql` in MySQL Workbench and execute the queries.

**7. Open Power BI**

Open `customer_dashboard.pbix` in Power BI Desktop and refresh the data connection.

---

## 📁 Project Structure

```
📦 customer-shopping-analysis
 ┣ 📓 customer_behaviour.ipynb     # Main Jupyter Notebook
 ┣ 📊 customer_shopping_behavior.xlsx  # Raw dataset
 ┣ 🗄️ customer_analysis.sql        # SQL queries
 ┣ 📈 customer_dashboard.pbix      # Power BI dashboard
 ┣ 📝 report.pdf                   # Written analysis report
 ┣ 🎞️ presentation.pdf             # Gamma presentation export
 ┗ 📄 README.md                    # This file
```



