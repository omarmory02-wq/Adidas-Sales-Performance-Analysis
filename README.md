# Adidas Sales Performance Analysis

## 📊 Project Overview

This project analyzes Adidas sales performance using **Python, Pandas, Power BI, Power Query, and DAX**. The goal is to explore sales and profitability data and transform it into meaningful business insights through data analysis and interactive visualization.

The dataset contains **1,200 transaction records** covering five global regions and three main product categories: Footwear, Apparel, and Accessories.

## 🎯 Project Objectives

* Analyze overall sales and profit performance
* Identify high-performing regions
* Compare product categories
* Analyze sales performance by store type
* Identify top-selling and profitable products
* Analyze units sold and revenue
* Calculate gross revenue and discount amounts
* Calculate profit margins
* Build an interactive Power BI dashboard
* Generate business insights from the data

## 🗂️ Dataset

The Adidas Sales Dataset was sourced from **Kaggle**.

### Main Columns

* `Order_ID`
* `Order_Date`
* `SKU`
* `Product_Name`
* `Category`
* `Region`
* `Store_Type`
* `Units_Sold`
* `Unit_Price`
* `Discount`
* `Revenue`
* `Profit`
* `Customer_Age`
* `Gender`
* `Payment_Method`

These fields were used to analyze sales, profitability, customers, products, regions, and sales channels.

## 🐍 Python Analysis

Python and Pandas were used to load the dataset and perform exploratory analysis.

```python
import pandas as pd

df = pd.read_csv('adidas_dataset_1200rows.csv')
df.head()
```

The analysis included grouping and aggregation by:

* Store Type
* Region
* Product
* Category

For example, sales-channel performance was calculated using Revenue, Profit, and Units Sold.

## 🧮 Calculated Columns

Three additional metrics were created during the analysis.

### Gross Revenue

```python
df['Gross_Revenue'] = df['Units_Sold'] * df['Unit_Price']
```

### Discount Amount

```python
df['Discount_Amount'] = (
    df['Gross_Revenue'] * (df['Discount'] / 100)
).round(2)
```

### Profit Margin

```python
df['Profit_Margin_%'] = (
    (df['Profit'] / df['Revenue']) * 100
).round(2)
```

These calculations provide additional information about the original value of sales, discounts, and profitability.

## 📈 Key Results

The dataset generated:

| Metric                |   Result |
| --------------------- | -------: |
| Total Revenue         | $287,380 |
| Total Profit          |  $85,070 |
| Total Units Sold      |    3,551 |
| Orders                |    1,200 |
| Average Profit Margin |   29.60% |

### Regional Performance

The analysis showed the following revenue and profit results:

| Region               |    Revenue |     Profit |
| -------------------- | ---------: | ---------: |
| Asia-Pacific         | $86,027.88 | $25,519.31 |
| North America        | $81,724.56 | $24,051.61 |
| Europe               | $69,057.16 | $20,403.56 |
| Latin America        | $32,966.34 |  $9,846.85 |
| Middle East & Africa | $17,601.98 |  $5,248.52 |

### Category Performance

| Category    |     Revenue |     Profit | Units Sold |
| ----------- | ----------: | ---------: | ---------: |
| Footwear    | $179,005.62 | $52,827.63 |      1,500 |
| Apparel     |  $77,377.83 | $22,056.46 |      1,022 |
| Accessories |  $30,994.47 | $10,185.76 |      1,028 |

### Sales Channel Performance

| Store Type |     Revenue |     Profit | Units Sold |
| ---------- | ----------: | ---------: | ---------: |
| Online     | $133,207.12 | $39,224.35 |      1,601 |
| Retail     | $102,147.08 | $30,288.41 |      1,263 |
| Outlet     |  $33,516.27 | $10,081.42 |        427 |
| Wholesale  |  $18,507.45 |  $5,475.67 |        259 |

## 🏆 Top Products

The analysis identified the following five products among the highest by revenue:

1. Predator Freak
2. Ultraboost Light
3. Primegreen Jacket
4. Copa Sense
5. Ultraboost 22

## 📊 Power BI Dashboard

An interactive **Power BI Executive Sales Performance Dashboard** was created to visualize:

* Revenue performance
* Profit performance
* Regional performance
* Product category performance
* Annual revenue trends
* Top profitable products
* Sales-channel performance

The dashboard provides an interactive way to explore the main findings from the analysis.

## 🛠️ Tools & Technologies

* **Python**
* **Pandas**
* **Jupyter Notebook**
* **Power Query**
* **Power BI**
* **DAX**
* **Microsoft Excel**
* **GitHub**

## 📁 Project Files

```text
Adidas-Sales-Performance/
│
├── Final_Project.ipynb
├── adidas_dataset_1200rows.csv
├── NTI PROJ.pbix
├── Final project Doc.docx
└── README.md
```

## 💡 Business Insights

The analysis provides a clear view of how Adidas sales vary across regions, categories, products, and sales channels. Footwear represents the largest category by revenue, while Online sales generate the highest revenue among the analyzed store types.

## 👨‍💻 Project Purpose

This project was developed as a practical **Data Analysis and Business Intelligence project**, demonstrating the process of loading data, analyzing it with Python and Pandas, creating calculated metrics, and presenting business insights through Power BI.

## 📌 Conclusion

The project demonstrates how raw sales data can be transformed into useful business information using Python and Power BI. The combination of data analysis, calculated metrics, and interactive visualization makes it possible to examine Adidas sales performance from multiple perspectives and support data-driven business analysis.

