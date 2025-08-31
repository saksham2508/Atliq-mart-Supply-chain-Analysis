# Atliq-mart-Supply-chain-Analysis
![banner](https://github.com/saksham2508/Atliq-mart-Supply-chain-Analysis/blob/main/project%20data/atliq%20mart%20supply%20chain%20project%20banner%20image.jpg)

## Project Overview
Atliq Mart, a growing FMCG manufacturer in Gujarat, faced **customer churn risks** as some key clients did not renew annual contracts due to **poor delivery performance**.  
The management wanted a **daily tracking system** for supply chain KPIs to identify service gaps and act quickly.  

This project delivers an **interactive Power BI dashboard** that monitors **On-Time (OT%), In-Full (IF%), OTIF%, Line Fill Rate (LIFR%), and Volume Fill Rate (VOFR%)**, with actionable insights for improving supply chain efficiency and retaining key customers.

---

## Company Background
- **Industry:** FMCG Manufacturer  
- **Headquarters:** Gujarat, India  
- **Current Operations:** Surat, Ahmedabad, Vadodara  
- **Expansion Goal:** Expand into Tier-1 cities within 2 years  
- **Business Challenge:**  
  - Customers not renewing contracts due to **late or incomplete deliveries**  
  - Need to track **OT%, IF%, and OTIF%** daily against customer-specific targets  

---

## Project Objective
- Track and improve **On-Time (OT%), In-Full (IF%), and OTIF%** delivery performance  
- Identify **delivery delays and fulfillment gaps** at customer, product, and city levels  
- Provide **actionable insights** for reducing service failures and customer churn  
- Build an **interactive Power BI dashboard** for management decision-making  

---

## Dataset & Data Model
The data was modeled into a **Star Schema** using fact and dimension tables:  

- **dim_customers** → Customer details (ID, Name, City)  
- **dim_products** → Product details (ID, Name, Category)  
- **dim_date** → Calendar table (Date, Month, Week No.)  
- **dim_targets_orders** → Target OT%, IF%, OTIF% per customer  
- **fact_order_lines** → Line-level order details (Qty Ordered, Delivered, Delivery Dates)  
- **fact_orders_aggregate** → Aggregated order-level KPIs (On-Time, In-Full, OTIF flags)  

---

## Key Metrics
- **OT% (On-Time %):** Orders delivered on/before agreed date  
- **IF% (In-Full %):** Orders delivered in full quantity  
- **OTIF%:** Orders delivered both On-Time and In-Full  
- **LIFR% (Line Fill Rate):** % of product lines fulfilled  
- **VOFR% (Volume Fill Rate):** % of total quantities delivered  

---

## Dashboard Overview

### 🔹 Order Level Dashboard
- KPI Cards: **Total Orders, OT Orders, IF Orders, OTIF Orders**  
- Gauge: OTIF% vs Target  
- City-wise OTIF% (Bar Chart)  
- Customer-wise performance (Matrix: OT%, IF%, OTIF%, LIFR%, VOFR%)  
- Metrics Trend over time (Line Chart)  
- Filters: Date, City, Customer
![Order Level](https://github.com/saksham2508/Atliq-mart-Supply-chain-Analysis/blob/main/Oreder%20level%20dashboard%20Image.png)

### 🔹 Line Level Dashboard
- KPI Cards: **Lines Ordered, Lines Filled, Volume Ordered, Volume Delivered**  
- Customer-wise LIFR% (Bar Chart)  
- LIFR% by Month & Customer (Matrix)  
- Product Category → LIFR vs VOFR (Clustered Chart)  
- LIFR Trend (Line Chart)  
- Filters: Date, Product, Customer
  ![Line Level](https://github.com/saksham2508/Atliq-mart-Supply-chain-Analysis/blob/main/line%20level%20dashboard%20image.png)

---

## Key Insights & Findings

### Overall Performance
- OT% and IF% are **30–35% below targets**; OTIF% only **29% vs 65.9% target**  
- Average delivery delay = **0.42 days**  
- No noticeable KPI improvements in recent months  

### Customer Insights
- **Lotus Mart**: Highest orders but lowest performance (OTIF = 16.34%, OT = 28.11%, IF = 53.35%, Avg cycle time = 1.28 days) → ⚠️ high churn risk  
- **Acclaimed Stores & Coolblue**: Also underperforming with long delays  
- **Propel Mart**: Best performer with cycle time = 0.15 days (almost same-day delivery)  

### Product Insights
- **Dairy** = most valuable category, followed by Food & Beverages  
- **Ghee, Curd, Butter** = most delayed products  
- **AM Milk 250** most ordered with minimal backlog, but **AM Milk 100** faces high backlog  

### Line vs Volume Fill Rate
- **VOFR ~96%** vs **LIFR ~66%** → Bulk SKUs delivered, but product lines incomplete  
- Customers with low LIFR: **Coolblue, Acclaimed, Lotus Mart, Elite Mart, Vijay Stores, Info Stores, Sorefoz Mart**  

---

## Recommendations
- **Customer Retention:**  
  - Focus on **Lotus Mart, Acclaimed Stores, Coolblue** to avoid churn  
  - Build **special SLAs and customer engagement strategy** for key accounts  

- **Delivery Improvements:**  
  - Reassess **delivery date estimation** and reduce scheduling delays  
  - Optimize logistics to reduce cycle time for large clients  

- **Product-Level Actions:**  
  - Strengthen **production & inventory planning** for Dairy products  
  - Solve backlog issues for **AM Milk 100** through demand forecasting  

- **KPI Monitoring:**  
  - Monthly KPI review for OT%, IF%, OTIF trends  
  - Dashboard-driven monitoring of customer-wise LIFR gaps  

---

## Conclusion
- Atliq Mart’s supply chain performance is **well below target levels**, risking customer churn.  
- Major clients (Lotus Mart, Acclaimed Stores, Coolblue) need **urgent focus** to retain contracts.  
- Dairy products (Ghee, Curd, Butter) cause delays → production & planning improvement required.  
- Despite high VOFR (96%), incomplete product lines (LIFR 66%) reduce customer satisfaction.  
- The Power BI dashboard provides **end-to-end visibility**, helping management take **data-driven actions** to improve service levels and support future expansion.  

---

## Tools & Technologies
- **Power BI** → Data Modeling, DAX, Dashboarding  
- **Excel/SQL** → Data Exploration & Validation  
- **Star Schema** → Fact & Dimension design  

---

## Author
**Saksham Singh**  
- Aspiring Data Analyst  
- [LinkedIn](https://www.linkedin.com/in/saksham-singh-3015b0265/)   

---
