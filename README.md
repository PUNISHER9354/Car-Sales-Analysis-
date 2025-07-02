# 🚗 Car Sales Analysis Dashboard – Power BI Project

This project is a comprehensive interactive dashboard built using **Power BI** to analyze and visualize car sales data. The dataset contains over 23,000 car listings with details like brand, model, price, buyer gender, body style, and dealer region.

![Dashboard Screenshot](https://github.com/PUNISHER9354/Car-Sales-Analysis-/blob/main/Car%20sales%20analysis%20dashboard%20screenshot%20.png)

---

## 📊 Features of the Dashboard

### 1. **KPIs and Summary Cards**
- 💰 **Max Car Price** – Highlights the most expensive listing.
- 🏢 **Top Selling Company** – Based on number of car listings.
- 🚘 **Top Selling Model** – Based on model-level sales.
- 🔢 **Total Cars Sold** – Total number of car entries.

### 2. **Demographic Analysis**
- 📈 Gender-based sales distribution (Pie + Bar Chart)
- 🧍 Buyer count by Gender

### 3. **Company & Model Analysis**
- 🏷️ Car sales by company and body style
- 📦 Top-selling car models
- 💸 Company-wise price comparison

### 4. **Time-based Trend**
- 📅 Car sales trend across months
- Filters available for **Month** and **Company**

---

## 🛠️ Tools & Technologies Used
- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Data Modeling**
- **Data Cleaning** (within Power BI)

---
Analysis-/blob/main/Car%20sales%20analysis%20dashboard%20screenshot%20.png
## 📁 Dataset Details
The dataset includes:
- `Car_id`, `Date`, `Customer Name`, `Gender`, `Annual Income`
- `Company`, `Model`, `Engine`, `Transmission`
- `Price ($)`, `Body Style`, `Dealer Region`, etc.

---
## screenshot
  ![Dashboard Preview](https://github.com/PUNISHER9354/Car-Sales-).
## 📌 Key DAX Measures
``` DAX
Total Cars = COUNT('CarsData'[Car_id])

Top Selling Company = 
VAR BrandSummary =
    SUMMARIZE('CarsData', 'CarsData'[Company], "Count", COUNTROWS('CarsData'))
VAR TopOne = TOPN(1, BrandSummary, [Count], DESC)
RETURN MAXX(TopOne, 'CarsData'[Company])

Top Selling Model = 
VAR ModelSummary =
    SUMMARIZE('CarsData', 'CarsData'[Model], "ModelCount", COUNTROWS('CarsData'))
VAR TopModel = TOPN(1, ModelSummary, [ModelCount], DESC)
RETURN MAXX(TopModel, 'CarsData'[Model])```



