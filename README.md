# 📊 Power BI Dashboards Portfolio

> Business Intelligence dashboards, DAX measures and KPI reporting for enterprise clients | Power BI • DAX • Azure

---

## 👩‍💻 About This Repository

This repository showcases my Power BI work including:
- 📈 Executive dashboards for enterprise clients
- 🏪 Business performance tracking for Walmart, Amazon & Home Depot
- 🔄 Migrated dashboards from Qlik to Power BI
- ⚡ Improved reporting latency by **40%**
- 🤖 Increased automation efficiency by **35%**

---

## 📂 Repository Structure
```
powerbi-dashboards/
│
├── 📁 dax-measures/
│   ├── revenue_measures.md
│   └── kpi_measures.md
│
├── 📁 dashboard-designs/
│   ├── business_performance_design.md
│   └── product_adoption_design.md
│
├── 📁 qlik-to-powerbi-migration/
│   └── migration_notes.md
│
└── README.md
```

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|---|---|
| Power BI Desktop | Dashboard design & development |
| DAX | Custom measures & calculations |
| Azure Data Factory | Data pipeline automation |
| Azure Databricks | Data transformation |
| SQL Server | Data source & modeling |

---

## 📌 Featured Dashboards

### 1️⃣ Enterprise Business Performance Dashboard
- Built for clients: **Walmart, Amazon, Home Depot**
- Tracks revenue, growth rate, operational KPIs
- Reduced reporting latency by **40%**

### 2️⃣ Product Adoption Dashboard
- Tracks feature adoption, MAU, funnel metrics
- Used by Product Managers for weekly reviews
- Built with drillthrough and dynamic slicers

### 3️⃣ Qlik to Power BI Migration
- Successfully migrated 15+ dashboards from Qlik
- Ensured 100% metric parity after migration
- Aligned all stakeholders during transition

### 4️⃣ Operational KPI Dashboard
- Real-time tracking of processing times
- Automated refresh via Azure Data Factory
- Increased automation efficiency by **35%**

---

## 💡 DAX Highlights
```dax
-- Total Revenue Measure
Total Revenue = SUMX(fact_transactions, [revenue])

-- Month over Month Growth
MoM Growth % = 
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], PREVIOUSMONTH(dim_date[date])),
    CALCULATE([Total Revenue], PREVIOUSMONTH(dim_date[date])),
    0
) * 100

-- Rolling 3 Month Average
Rolling 3M Avg Revenue = 
CALCULATE(
    AVERAGE(fact_transactions[revenue]),
    DATESINPERIOD(dim_date[date], LASTDATE(dim_date[date]), -3, MONTH)
)
```

---

## 📜 Certifications
✅ Microsoft Certified: Power Platform Functional Consultant Associate (PL-200)

---

## 🤝 Connect with Me
- 💼 [LinkedIn](https://linkedin.com/in/sadhana-s-kumar)
- 📧 sanasadhana07@gmail.com
- 🐙 [GitHub Profile](https://github.com/sadhana007)
