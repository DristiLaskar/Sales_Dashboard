# 📈 E-commerce Sales Analysis Dashboard (Power BI)

A comprehensive Power BI dashboard that transforms raw e-commerce sales data into an interactive and insightful report. This project analyzes key performance indicators (KPIs) across sales, profit, product categories, and geographical locations to drive data-driven business decisions.

<p align="center">
  <img alt="Power BI" src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
  <img alt="Data Analysis" src="https://img.shields.io/badge/Data_Analysis-Visual-blue?style=for-the-badge&logo=chartmogul"/>
  <img alt="Dataset" src="https://img.shields.io/badge/Dataset-CSV-orange?style=for-the-badge&logo=files"/>
</p>

---

## 📋 Table of Contents

- [Dashboard Showcase](#-dashboard-showcase)
  - [Sales Overview](#-sales-overview)
  - [Profit Analysis](#-profit-analysis)
- [✨ Key Features & KPIs](#-key-features--kpis)
- [💾 Data Model](#-data-model)
- [🛠️ Technologies Used](#️-technologies-used)
- [🚀 How to Use](#-how-to-use)

---

## 📊 Dashboard Showcase

Here are the two main pages of the interactive report, providing a complete picture of business performance.

### 💰 Sales Overview

This page focuses on top-line revenue, customer behavior, and sales performance by category and location.

<p align="center">
  <img src="Screenshot 2025-10-23 201615.png" alt="Sales Analysis Dashboard" width="90%">
</p>

### 💸 Profit Analysis

This page dives deeper into profitability, analyzing profit margins, and identifying the most and least profitable areas of the business.

<p align="center">
  <img src="Screenshot 2025-10-23 201951.png" alt="Profit Analysis Dashboard" width="90%">
</p>

---

## ✨ Key Features & KPIs

This dashboard tracks the most critical metrics for an e-commerce business:

* **📈 Total Sales:** $2.29M
* **💰 Total Profit:** $0.24M
* **📦 Total Quantity Sold:** 13.7K
* **📊 Profit Margin:** 10.43%

**Interactive Visualizations:**

* **Slicers:** Dynamically filter the entire report by **Category** and **Year**.
* **Line Chart:** Track **Total Profit by Month** to identify seasonal trends.
* **Bar Charts:**
    * Identify **Top 5 States by Sales**.
    * Analyze **Sales & Profit by Sub-Category**.
* **Donut/Pie Charts:**
    * Break down **Sales & Profit by Category** (Clothing, Electronics, Furniture).
    * Understand **Sales & Profit by Payment Mode** (COD, EMI, UPI, Credit Card).
* **Table:** View the **Top 5 Customers** by sales.

---

## 💾 Data Model

The report is built on a simple relational model using two CSV files, connected by `Order ID`.

* **`Orders.csv` (Dimension Table):** Contains details about each order's customer and location.
* **`Details.csv` (Fact Table):** Contains transaction-level data for each order.

```
+----------------+      +----------------+
|    Orders.csv  |      |   Details.csv  |
|----------------|      |----------------|
| ✅ Order ID (PK) | 1..* | ✅ Order ID (FK) |
|  Order Date    |      |  Amount        |
|  CustomerName  |      |  Profit        |
|  State         |      |  Quantity      |
|  City          |      |  Category      |
+----------------+      |  Sub-Category  |
                        |  PaymentMode   |
                        +----------------+
```

---

## 🛠️ Technologies Used

* **Microsoft Power BI:** The primary tool for data modeling, analysis, and visualization.
* **Power Query (M Language):** Used for Extract, Transform, Load (ETL) operations to clean and prepare the data.
* **DAX (Data Analysis Expressions):** Used to create custom measures like `Total Sales`, `Total Profit`, and `Profit Margin`.

---

## 🚀 How to Use

To explore this report:

1.  **Download the files:**
    * Download the `.pbix` file (the main Power BI report).
    * Download the `Orders.csv` and `Details.csv` data files.
2.  **Open in Power BI Desktop:**
    * Open the `.pbix` file.
3.  **Update Data Source (If needed):**
    * If the report can't find the CSV files, go to `Transform data` -> `Data source settings`.
    * Select `Change Source...` for each CSV and browse to the location where you saved them on your computer.
4.  **Interact:**
    * Click on any chart, slicer, or table to filter and explore the data.
