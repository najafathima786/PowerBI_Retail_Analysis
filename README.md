# PowerBI_Retail_Analysis
To perform interactive sales analytics using Power BI by connecting and transforming multiple retail datasets. The goal is to uncover actionable insights around revenue, customer distribution, and cancellations through visual dashboards.
# Power BI Retail Analysis

## 📖 Overview
This Power BI project analyzes retail data by managing multiple tables, creating relationships, and using DAX formulas to enhance the dataset. The objective is to generate insights into sales, customer distribution, and cancellation trends through interactive dashboards.

---

## 🏢 Business Context
The goal of this project is to simulate a business case where retail sales data is analyzed for KPIs like revenue, units sold, cancellations, and customer behavior. It involves integrating multiple datasets and generating dashboards to help business stakeholders make data-driven decisions.

---

## 📊 Dataset Description

The dataset consists of the following tables:

- **PinCode-Geo**: Contains geographic data such as city, zone, and pincode.
- **Mod3_Raw_CityTier**: Provides information on city tiers.
- **Sales Raw**: Includes transaction details like order date, revenue, units sold, and cancellations.
- **Mod3_Raw_ProductMaster**: Contains product-related information.

---

## 🔧 Data Cleaning & Transformation

Steps performed:
- Dropped records from PinCode-Geo where Zone is missing.
- Removed records from Mod3_Raw_CityTier where CityTier is missing.
- Established relationships between common columns (e.g., City in both Mod3_Raw_CityTier and PinCode-Geo).
- Created calculated columns using DAX:
  - Net_Units = 'Sales Raw'[Units] - 'Sales Raw'[Cancelled_Units]
  - OrderDayOfWeek = FORMAT('Sales Raw'[OrderDate].[Day], "dddd")
  - OrderWeekStart = FORMAT(('Sales Raw'[OrderDate] - WEEKDAY('Sales Raw'[OrderDate], 2) + 1), "mmm dd")
  - Total_Revenue = CALCULATE(SUM('Sales Raw'[Revenue]), 'Sales Raw'[Net_Units] > 0)

---

## 📈 Key Metrics & KPIs

| Metric              | Value     |
|---------------------|-----------|
| Total Revenue       | $38.84M   |
| Total Customers     | 83K       |
| Total Transactions  | 84.76K    |
| Net Units Sold      | 60.33K    |

---

## 🧠 Insights Generated

- Revenue and Transactions trends across months and weekdays
- Zone-wise and City Tier performance
- Cancellation and net unit trends
- High-performing cities and products

---

## 📊 Power BI Dashboard Features

### Dashboard 1: City-wise Analysis
- Visuals: Bar charts, pie charts, treemaps
- Filters: City, Zone, City Tier
- Focus: Customer & revenue distribution by city

### Dashboard 2: Date-wise Analysis
- Visuals: Line charts, column charts
- Focus: Monthly and weekly trends, order days, cancellations
<img width="1442" height="874" alt="Dashboard_!" src="https://github.com/user-attachments/assets/72e52fd0-08b4-4baa-8311-2485fee6c1b7" /><img width="1444" height="875" alt="Dasgboard_2" src="https://github.com/user-attachments/assets/1d74ad31-9151-4ec8-90fb-873fe1304241" />


## 🛠 Tools & Technologies Used
- Power BI Desktop
- DAX (Data Analysis Expressions)
- GitHub (for project sharing)

---

## 📂 Repository Contents

| File Name               | Description                           |
|-------------------------|---------------------------------------|
| Retail_Analysis.pbix  | Power BI report file                  |
| City_Analysis.png     | Screenshot of city-wise dashboard     |
| Date_Analysis.png     | Screenshot of date-wise dashboard     |
| README.md             | Project documentation (this file)     |

---

## 🚀 How to Use

1. Clone or download the repository.
2. Open Retail_Analysis.pbix in Power BI Desktop.
3. Use the slicers and filters to explore data insights.
4. Refer to the .png images for quick overviews.

---

## 📬 Contact
For questions or collaboration, feel free to open an issue or connect via GitHub. how too save this file
