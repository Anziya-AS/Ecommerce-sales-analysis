# 🛒 Ecommerce Sales Analysis

A business intelligence project analyzing an e-commerce dataset to uncover sales trends, customer behavior, and revenue insights using Power BI.

---

## 🎯 Objective

To analyze ecommerce performance and assist in data-driven decision making by identifying key metrics like total sales, returning customers, and top-performing products & cities.

---

## 🛠 Tools Used

- **Power BI** – Dashboard development  
- **Excel** – Data cleaning and transformation  
- **DAX** – For custom measures and KPIs  

---

## 📂 Dataset

The dataset includes:
- Sales transactions  
- Customer details  
- Product categories  
- Region, segment, and shipping details  

📎 [Google Sheet Dataset](https://docs.google.com/spreadsheets/d/1zMoqDjJc9LD9g__K_7FchFot3f-sH-HU/edit?usp=sharing)

---

## 📌 Key Insights

- 📈 **Revenue increased** by over 30% in Q4 compared to Q1  
- 💻 **Laptops, Phones, and Tablets** made up 60% of total sales revenue  
- 🌐 **Top-performing cities**: Mumbai, Bangalore, and Delhi  
- 🧾 **Average order value** was highest in the Corporate segment  
- 🔁 **Returning customers** accounted for 45% of total orders  

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
    DATESMTD('Sales'[Order_Date])
)




---

