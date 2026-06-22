# Supply Chain & Inventory Analytics

## Project Overview

This project analyzes a global supply chain dataset to evaluate sales performance, profitability, delivery efficiency, customer segments, and market performance. Using Python, SQL, and Power BI, the analysis identifies operational bottlenecks and revenue opportunities across markets, products, and shipping methods.

**Dataset Size:** 180,519 records | 47 analytical columns

**Tools Used:** Python (Pandas), SQL, Power BI

---

## Business Questions

* Which markets generate the highest revenue and profit?
* Which product categories contribute the most to business performance?
* How significant is the late delivery problem?
* Which customer segments drive profitability?
* How do shipping methods impact operational performance?
* What trends can be observed in sales and profit over time?

---

## Dashboard Preview

![Dashboard](sales_dashboard.png)

---

## Key Business Insights

### Market Performance

* Europe generated the highest overall profit, followed closely by LATAM.
* Revenue and profitability were concentrated within a few major markets.
* Market ranking analysis highlighted regions with the strongest business contribution.

### Product Performance

* Fishing, Cleats, and Camping & Hiking were the highest-performing categories in both revenue and profit.
* Several categories generated sales but contributed relatively low profit, indicating margin optimization opportunities.

### Delivery Performance

* Approximately **55% of orders experienced late delivery risk**.
* Late deliveries remained consistently high across all markets.
* Delivery efficiency represents one of the largest operational improvement opportunities.

### Customer Segment Analysis

* Consumer customers generated the highest revenue and profit contribution.
* Corporate and Home Office segments represented valuable secondary revenue streams.

### Shipping Analysis

* Standard Class handled the majority of shipments.
* First Class shipping produced the highest average profit per order.
* Shipping method selection had a measurable impact on profitability and delivery outcomes.

---

## Sample SQL Analysis

### Market Revenue Ranking (Window Function)

```sql
SELECT
    Market,
    ROUND(SUM(Sales),2) AS Revenue,
    RANK() OVER(
        ORDER BY SUM(Sales) DESC
    ) AS Revenue_Rank
FROM orders_staging
GROUP BY Market;
```

---

## Skills Demonstrated

* Data Cleaning & Transformation
* Exploratory Data Analysis (EDA)
* SQL Aggregations & Window Functions
* Supply Chain Analytics
* Profitability Analysis
* Delivery Performance Analysis
* Customer Segmentation
* KPI Development
* Power BI Dashboard Design
* Business Insight Generation

---

## Project Files

* [Power BI Dashboard](Ecommerce_performance_analysis.pbix)
* [SQL Analysis](supply_chain_analysis.sql)
* [Cleaned Dataset](supply_chain_analytics_dataset.csv)

---

## Business Impact

The analysis revealed that late delivery risk affects more than half of all orders, while profitability is heavily concentrated in specific markets and product categories. These insights can support improvements in logistics performance, inventory planning, shipping strategy, and market-level decision-making.
