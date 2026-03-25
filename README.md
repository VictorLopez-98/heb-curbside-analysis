# H-E-B Curbside KPI Analysis

## Overview
This project analyzes H-E-B curbside performance using KPI reports.  
The focus is on department growth, store performance, fulfillment methods, and operational efficiency metrics.

The goal is to convert raw operational reports into structured data and generate insights using SQL and Python.

---

## Data Sources
This project is based on KPI report data including:
- Department growth (Bakery, Produce, Grocery, etc.)
- Store performance metrics (orders, sales, wait time)
- Fulfillment ratings:
  - Pickup (PU): 4.68  
  - Order Ahead (OA): 4.37  
  - Home Delivery (HD): 5.00  

- Operational metrics:
  - Subs/Shorts Order %: 32.8%  
  - Subs/Shorts Line Item %: 3.3%  
  - Immediacy %: 0.0%  
  - POR (Order Accuracy): 4.5  

---

## Objectives
- Analyze department growth performance  
- Track key store KPIs  
- Compare fulfillment methods (PU, OA, HD)  
- Evaluate operational efficiency (subs/shorts, accuracy)  
- Build a structured relational database  

---

## Tools & Technologies
- Python (Pandas)  
- SQL (MySQL)  
- VS Code  
- Git & GitHub  

---

## 📁 Project Structure

```
heb-curbside-analysis/
├── data/                  # Raw KPI data
├── Analysis.py            # Python analysis script
├── schema.sql             # Database schema
├── README.md              # Documentation
```

---

## Database Design

### 1. reports
Stores overall store KPI metrics.

- report_id (Primary Key)
- store_name
- avg_wait_time
- order_count
- sales
- items
- penetration

---

### 2. department_growth
Tracks department-level growth.

- growth_id (Primary Key)
- report_id (Foreign Key)
- department_name
- growth_percent

---

### 3. fulfillment_metrics
Stores fulfillment performance ratings.

- metric_id (Primary Key)
- report_id (Foreign Key)
- fulfillment_type (PU, OA, HD)
- rating

---

### 4. operational_metrics
Tracks operational efficiency KPIs.

- op_id (Primary Key)
- report_id (Foreign Key)
- metric_name
- metric_value

Includes:
- Subs/Shorts Order %
- Subs/Shorts Line Item %
- Immediacy %
- POR (Order Accuracy)

---

## Relationships
- One report → many department growth records  
- One report → many fulfillment metrics  
- One report → many operational metrics  

---

## Key Insights (Example)
- Bakery shows the highest department growth  
- Home Delivery has the highest fulfillment rating  
- Order Ahead shows lower performance compared to other methods  
- Subs/Shorts metrics highlight operational inefficiencies  
- POR (Order Accuracy) reflects overall service quality  

---

## Future Improvements
- Add weekly KPI trend data  
- Build dashboards (Power BI / Tableau)  
- Automate data updates  
- Expand dataset for long-term analysis  

---

## Author
Victor Lopez  
