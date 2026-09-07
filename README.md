# Sales_Dashboard_Project
A tailored README.md generated specifically for your e-commerce dataset (Details.csv and Orders.csv) with the dark aesthetic canvas provided:
# 📊 E-Commerce Sales Analytics Dashboard

A modern, dark-themed Power BI / Data Analytics dashboard designed to analyze transaction trends, profitability, customer locations, and payment preferences across Indian states.

![Dashboard Preview](dark-gradient.jpg)

---

## 📌 Executive Summary
This project analyzes **500 unique orders** across **19 states** in India during 2018, combining transactional order breakdowns with geographic customer demographics to deliver key financial and operational insights.

### 🎯 Key Performance Indicators (KPIs)
* **Total Sales Revenue:** ₹4,37,771
* **Total Profit:** ₹36,963
* **Total Quantity Sold:** 5,615 units
* **Product Categories:** Electronics, Clothing, Furniture

---

## 📁 Repository Structure
```text
├── data/
│   ├── Details.csv          # Transactional details (Amount, Profit, Category, Payment Mode)
│   └── Orders.csv           # Customer & Location details (Order Date, Customer Name, State, City)
├── assets/
│   └── dark-gradient.jpg    # Custom canvas background theme
├── Sales_Dashboard.pbix     # Interactive Power BI report file
└── README.md                # Project documentation

```python
import pandas as pd

# Load datasets
details = pd.read_csv('Details.csv')
orders = pd.read_csv('Orders.csv')

print("Details Columns:", details.columns.tolist())
print("Details Head:\n", details.head(2))
print("\nOrders Columns:", orders.columns.tolist())
print("Orders Head:\n", orders.head(2))


```

```text
Details Columns: ['Order ID', 'Amount', 'Profit', 'Quantity', 'Category', 'Sub-Category', 'PaymentMode']
Details Head:
   Order ID  Amount  Profit  Quantity     Category      Sub-Category PaymentMode
0  B-25681    1096     658         7  Electronics  Electronic Games         COD
1  B-26055    5729      64        14    Furniture            Chairs         EMI

Orders Columns: ['Order ID', 'Order Date', 'CustomerName', 'State', 'City']
Orders Head:
   Order ID  Order Date CustomerName          State     City
0  B-26055  10-03-2018    Harivansh  Uttar Pradesh  Mathura
1  B-25993  03-02-2018       Madhav          Delhi    Delhi


```

```python
# Merge to inspect aggregate values
df = pd.merge(details, orders, on='Order ID', how='inner')
print("Total Orders:", df['Order ID'].nunique())
print("Total Revenue (Amount):", df['Amount'].sum())
print("Total Profit:", df['Profit'].sum())
print("Total Quantity:", df['Quantity'].sum())
print("Categories:", df['Category'].unique().tolist())
print("States Count:", df['State'].nunique())
print("Min Date:", df['Order Date'].min(), "Max Date:", df['Order Date'].max())


```

```text
Total Orders: 500
Total Revenue (Amount): 437771
Total Profit: 36963
Total Quantity: 5615
Categories: ['Electronics', 'Clothing', 'Furniture']
States Count: 19
Min Date: 01-01-2018 Max Date: 31-12-2018


```

A tailored `README.md` generated specifically for your e-commerce dataset (`Details.csv` and `Orders.csv`) with the dark aesthetic canvas provided:

```markdown
# 📊 E-Commerce Sales Analytics Dashboard

A modern, dark-themed Power BI / Data Analytics dashboard designed to analyze transaction trends, profitability, customer locations, and payment preferences across Indian states.

![Dashboard Preview](dark-gradient.jpg)

---

## 📌 Executive Summary
This project analyzes **500 unique orders** across **19 states** in India during 2018, combining transactional order breakdowns with geographic customer demographics to deliver key financial and operational insights.

### 🎯 Key Performance Indicators (KPIs)
* **Total Sales Revenue:** ₹4,37,771
* **Total Profit:** ₹36,963
* **Total Quantity Sold:** 5,615 units
* **Product Categories:** Electronics, Clothing, Furniture

---

## 📁 Repository Structure
```text
├── data/
│   ├── Details.csv          # Transactional details (Amount, Profit, Category, Payment Mode)
│   └── Orders.csv           # Customer & Location details (Order Date, Customer Name, State, City)
├── assets/
│   └── dark-gradient.jpg    # Custom canvas background theme
├── Sales_Dashboard.pbix     # Interactive Power BI report file
└── README.md                # Project documentation

```

---

## 🛠️ Data Model & Schema

The dataset consists of two relational tables joined by **`Order ID`**:

* **`Details.csv`**: `Order ID`, `Amount`, `Profit`, `Quantity`, `Category`, `Sub-Category`, `PaymentMode` (COD, EMI, Credit Card, Debit Card, UPI).
* **`Orders.csv`**: `Order ID`, `Order Date`, `CustomerName`, `State`, `City`.

---

## 📈 Dashboard Key Visualizations & Insights

1. **Category & Sub-Category Performance:**
* Visualizes profit margin and sales performance across **Clothing**, **Electronics**, and **Furniture**.


2. **Geographic Distribution:**
* Map and bar visualizations breakdown order volume and revenue across **19 states** and major cities.


3. **Payment Mode Breakdown:**
* Analysis of customer purchasing habits (COD, EMI, UPI, Credit Card, Debit Card).


4. **Monthly Sales Trends:**
* Order volume and revenue trajectories throughout the 2018 operational calendar year.


## 🚀 How to Replicate or Run

1. **Clone the repository:**
```bash
git clone [https://github.com/your-username/sales-analytics-dashboard.git](https://github.com/your-username/sales-analytics-dashboard.git)

```


2. **Open Power BI:**
* Open `Sales_Dashboard.pbix` in Power BI Desktop.


3. **Apply Dark Theme:**
* Use `dark-gradient.jpg` under **Page Canvas Background** with **0% transparency** and **Fit** image fit mode.



```

```
