# 📊 Data Analytics with Power BI — Superstore Analysis

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://www.microsoft.com/excel)
[![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-orange?style=for-the-badge)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

An end-to-end Business Intelligence (BI) and data analytics project built with **Microsoft Power BI** and **Microsoft Excel**, analyzing commercial performance, sales trends, regional distribution, and customer segmentation for a retail superstore.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset Architecture](#-dataset-architecture)
- [Dashboard & Visualizations Breakdown](#-dashboard--visualizations-breakdown)
- [Key Insights & Analytics Deliverables](#-key-insights--analytics-deliverables)
- [Prerequisites & Getting Started](#-prerequisites--getting-started)
- [Tech Stack & Tools](#-tech-stack--tools)
- [Future Enhancements](#-future-enhancements)

---

## 🔍 Project Overview

The objective of this project is to transform raw retail transaction data into actionable business intelligence using **Power BI Desktop**. It provides comprehensive reporting on:

- **Sales Performance**: Total sales revenue aggregated across regions and customer segments.
- **Time-Series Analysis**: Annual, quarterly, monthly, and daily trends using date hierarchies.
- **Comparative & Structural Analysis**: Utilizing multiple visualization paradigms (Ribbon, Waterfall, Funnel, Gauge, Clustered/Stacked Columns, and Donut charts) to reveal sales dynamics and regional rankings over time.

---

## 🗄️ Dataset Architecture

The project leverages the **Super Store Dataset** (`Dataset/Dataset.xlsx`), organized into three interconnected relational tables:

| Sheet Name | Description | Key Attributes / Fields |
|:---|:---|:---|
| **`Orders`** | Granular retail order transactions | `Order ID`, `Order Date`, `Ship Date`, `Ship Mode`, `Customer ID`, `Customer Name`, `Segment`, `City`, `State`, `Region`, `Product ID`, `Category`, `Sub-Category`, `Product Name`, `Sales` |
| **`Returns`** | Order return logs | `Returned`, `Order ID` |
| **`People`** | Regional management directory | `Person` (Regional Lead), `Region` (East, West, Central, South) |

---

## 📈 Dashboard & Visualizations Breakdown

The Power BI report (`Working File/Super Store Analysis with Dashboard.pbix`) is structured into dedicated analytical views to explore different dimensions of sales performance:

### 1. 📊 Bar & Column Charts
- **Standard Column Charts**: Total sales revenue distribution across geographical regions (`Region`).
- **Clustered & Stacked Column Charts**: Multi-dimensional breakdown of sales by `Region` cross-tabulated with customer segments (`Consumer`, `Corporate`, `Home Office`).
- **100% Stacked Column Chart**: Proportional share analysis of customer segments per region.

### 2. 📉 Line Chart
- **Historical Sales Trajectory**: Time-series progression tracking sales across dynamic Date Hierarchies (`Year` ➔ `Quarter` ➔ `Month` ➔ `Day`).
- **Multi-Line Regional Comparison**: Trend line overlay comparing sales growth and seasonal spikes across the West, East, Central, and South regions simultaneously.

### 3. 🎀 Ribbon Chart
- **Dynamic Regional Rankings**: Visualizes how regional sales leadership shifts over quarters and years, highlighting fluctuations in market dominance and strategic growth periods.

### 4. 🌊 Waterfall Chart
- **Sales Progression & Variance**: Deconstructs cumulative sales growth over time with categorical breakdown by region, illustrating positive and negative regional contributions.

### 5. 🔻 Funnel Chart
- **Regional Sales Volume Hierarchy**: Visual representation of total sales ranked from highest-performing to lowest-performing market territories.

### 6. 🍩 Pie & Donut Charts
- **Market Share Distribution**: Proportional composition of overall retail sales by geographic region, identifying core revenue-generating territories.

### 7. 🎯 Gauge Chart
- **KPI & Target Attainment**: Executive metric gauge evaluating aggregate sales performance against predefined enterprise targets and thresholds.

---

## 💡 Key Insights & Analytics Deliverables

- **Segment Dominance**: Identification of top revenue-driving customer segments across various regional demographics.
- **Seasonality & Trends**: Clear identification of cyclical sales peaks, particularly during year-end shopping seasons.
- **Territory Benchmarking**: Comparative visibility into underperforming vs. high-performing regions to support regional manager resource allocation.

---

## 🚀 Prerequisites & Getting Started

### Prerequisites
- [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Free download, Windows)
- Microsoft Excel (optional, for inspecting the raw data)

### How to Run Locally

1. **Clone the repository**:
   ```bash
   git clone https://github.com/bhattchintan8540-cmd/Data-Analytics-with-Power-BI.git
   ```

2. **Open the Power BI file**:
   - Navigate to `Working File/`
   - Double-click `Super Store Analysis with Dashboard.pbix` to launch the interactive dashboard in Power BI Desktop.

3. **Refresh or modify the data**:
   - In Power BI Desktop, click **Transform Data** under the Home tab to inspect applied Power Query transformation steps.
   - Click **Refresh** to reload data from `Dataset/Dataset.xlsx`.

---

## 🛠️ Tech Stack & Tools

- **Business Intelligence**: Microsoft Power BI Desktop
- **Data Modeling & Queries**: Power Query (M Language), DAX
- **Data Source**: Microsoft Excel (`.xlsx`)
- **Version Control**: Git & GitHub

---

## 🔮 Future Enhancements

- [ ] Incorporate profit margin, discount impact, and shipping cost calculations.
- [ ] Add interactive slicers and cross-filtering navigation buttons across all dashboard pages.
- [ ] Implement DAX-based Year-over-Year (YoY) and Quarter-over-Quarter (QoQ) growth measures.
- [ ] Export high-resolution snapshots/PDF reports into the `Dashboard/` folder.

---
*⭐ If you find this repository helpful, consider giving it a star!*
