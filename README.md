# 🏪 Convenience Store Data Analytics & Looker Studio Dashboard

## 📌 Project Overview
This project provides an end-to-end data analytics solution designed to transform raw convenience store transaction logs into actionable business intelligence. Leveraging **Google BigQuery (SQL)** for data transformation and **Google Looker Studio** for visual reporting, this project replicates enterprise-level analytics tailored for retail operations.

The analysis focuses on three core business vectors:
1. **Inventory & Product Velocity:** Isulating array-based basket items to find total revenue contributions.
2. **Labor & Operational Efficiency:** Mapping peak customer foot traffic by hour to optimize store staffing.
3. **Marketing ROI:** Evaluating customer demographic responses to active promotional campaigns.

👉 **[Click here to view the Live Interactive Looker Studio Dashboard]()**    << ** >>

---

## 🧠 Business Context & Core Analytical Framework
My analytical approach is heavily informed by a combined professional background:
* **Retail Business Ownership (4 Yrs):** Understanding inventory holding costs, high-margin categories, and the direct impact of promotional waste on bottom-line retail net revenue.
* **Amazon Fulfillment Operations (5 Yrs):** Applying supply chain principles regarding product velocity, high-volume logistics throughput, and processing efficiency.
* **Senior Software QA Engineering (12 Yrs):** Ensuring structural data integrity, validating schema constraints, and edge-case error handling (such as raw string-to-array conversions).

---

## 🛠️ Tech Stack & Methods Used
* **Data Warehouse:** Google BigQuery
* **SQL Techniques:** Regular Expressions (`REGEXP_REPLACE`), String Parsing (`SPLIT`), Array Flattening (`UNNEST`), Time Conversions (`EXTRACT`), and Conditional Aggregations (`SAFE_DIVIDE`).
* **BI Visualization:** Google Looker Studio (Dual-Axis Charts, 100% Stacked Matrixes, Treemaps).

---

## 📂 Repository Structure
convenience-store-analytics/
├── README.md               
├── data/
│   └── schema.md           <-- Detailed Schema Definitions & Data Types
├── sql_queries/
│   ├── 01_product_popularity.sql
│   ├── 02_hourly_traffic_peaks.sql
│   └── 03_demographics_promotions.sql
└── visuals/
    ├── combo_chart_sales.png
    ├── stacked_bar_promotions.png
    └── treemap_payment_methods.png
```

---

## 📊 Dashboard Visualizations & Key Insights

### 1. Revenue Velocity vs. Customer Foot Traffic
Tracks transaction counts against overall revenue spikes across seasonal intervals to differentiate between high-margin shopping trips and high-volume baseline traffic days.
[![Sales Velocity](visuals/combo_chart_sales.png)](REPLACE_WITH_YOUR_LOOKER_STUDIO_SHARE_LINK)  <<  ** >>

### 2. Campaign Attractiveness Matrix (100% Stacked Bar)
Isolates which age and demographic categories respond best to specific types of discount frameworks (e.g., BOGO vs. flat discounts).
[![Promotion Matrix](visuals/stacked_bar_promotions.png)](REPLACE_WITH_YOUR_LOOKER_STUDIO_SHARE_LINK)                                   << ** >>

### 3. Operational Payment Flow Treemap
A visual breakdown mapping payment types alongside customer loyalty card penetration to track digital wallet adaptation rates.
[![Payment Flow](visuals/treemap_payment_methods.png)](REPLACE_WITH_YOUR_LOOKER_STUDIO_SHARE_LINK)                                     << ** >>

---

## 💻 SQL Query Deep Dives

### Query 1: Unnesting Product Arrays for Velocity Check
Because the raw data stored retail basket products inside an array represented as a text string (e.g., `['Tea', 'Sandals']`), standard groupings failed. This query sanitizes the string, converts it to an array type, and flattens it for accurate aggregation.

*The full SQL script can be viewed in [`sql_queries/01_product_popularity.sql`](sql_queries/01_product_popularity.sql).*             << ** >> 

---

## 💡 Key Actionable Recommendations for Store Managers
1. **Staffing Optimization:** Shift employee schedules forward by 2 hours based on peak afternoon traffic identified in Query 2 to reduce front-counter wait times and drop checkout cart abandonment.
2. **Targeted Merchandising:** Group high-affinity items uncovered in the unnested product lists next to high-traffic endcaps to trigger impulse buying behavior.
3. **Promotion Adjustments:** Discontinue low-performing promotion types among loyalty tiers to preserve margins.

---
**Contact:** Himansu Desai | LinkedIn URL: https://www.linkedin.com/in/himansu-desai/                                                        
