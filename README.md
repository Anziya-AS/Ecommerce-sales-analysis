# 🛒 E-Commerce Sales Analysis

A complete end-to-end project using Python, SQL, Excel, and Power BI to analyze e-commerce retail data, identify key business insights, and visualize sales performance across various segments.

---

## 📌 Objective

This project aims to:
- Analyze monthly revenue trends
- Identify top-performing products and regions
- Segment customers based on behavior
- Visualize results in an interactive dashboard

---

## 🛠 Tools & Technologies

- **Python** – Data cleaning and exploratory analysis (Pandas, Seaborn, Matplotlib)
- **SQL** – Business logic and aggregations (MySQL)
- **Excel** – Data pre-processing and initial exploration
- **Power BI** – Dashboard creation and KPIs

---

## 📁 Project Structure
ecommerce-sales-analysis/
├── data/
│ └── sales_data.csv
├── notebooks/
│ └── data_cleaning_analysis.ipynb
├── sql/
│ └── sales_queries.sql
├── dashboard/
│ ├── sales_dashboard.pbix
│ └── sales_dashboard.pdf
├── README.md


---

## 📊 Key Insights

- 📈 **Revenue increased** by over 30% in Q4 compared to Q1.
- 🛍️ **Laptops, Phones, and Tablets** made up 60% of total sales revenue.
- 🌍 **Top-performing cities**: Mumbai, Bangalore, and Delhi.
- 🧾 **Average order value** was highest in the Corporate segment.
- 🧠 Returning customers accounted for 45% of total orders.

---

## 🧠 Key DAX Measures (Power BI)

```DAX
-- Total Revenue
Total Sales = SUM('Sales'[Sales_Amount])

-- Average Order Value
Average Order Value = AVERAGE('Sales'[Order_Value])

-- Returning Customers Count
Returning Customers = 
CALCULATE(
    DISTINCTCOUNT('Sales'[Customer_ID]),
    'Sales'[IsReturning] = "Yes"
)

-- Monthly Sales Trend
Monthly Sales = 
CALCULATE(
    SUM('Sales'[Sales_Amount]),
    ALLEXCEPT('Sales', 'Sales'[Month])
)
-- Total Sales
SELECT SUM(Sales_Amount) AS Total_Sales FROM sales_data;

-- Top 5 Products
SELECT Product, SUM(Sales_Amount) AS Revenue
FROM sales_data
GROUP BY Product
ORDER BY Revenue DESC
LIMIT 5;

-- Monthly Sales
SELECT DATE_FORMAT(Order_Date, '%Y-%m') AS Month, SUM(Sales_Amount) AS Monthly_Sales
FROM sales_data
GROUP BY Month;
## 📊 Dashboard

Created in Power BI using slicers, cards, maps, and bar charts.  
Includes KPIs for revenue, AOV, top products, and regions.



---

## 👩‍💻 Created By

**Anziya A S**  
🔍 Software Engineer & Data Analyst  
📫 anziyaanzarr90@gmail.com  
📍 Kerala, India  
🔗 [GitHub Profile](https://github.com/Anziya-AS)
