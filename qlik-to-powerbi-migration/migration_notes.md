# 🔄 Qlik to Power BI Migration

> Author: Sadhana S Kumar
> Description: Notes and approach for migrating
>              dashboards from Qlik Sense to Power BI

---

## 📋 Project Overview

| Item | Details |
|---|---|
| 📅 Timeline | Jul 2024 – Present |
| 🏢 Company | FirstAdvantage, Bengaluru |
| 📊 Dashboards Migrated | 15+ enterprise dashboards |
| 👥 Stakeholders | Product Managers, Business Teams |
| ✅ Outcome | 100% metric parity, 40% faster reporting |

---

## 🗺️ Migration Approach

### Step 1 — Audit Existing Qlik Dashboards
- Document all existing Qlik dashboards
- List every metric, filter and visualization
- Identify data sources and connections
- Flag complex calculated fields

### Step 2 — Map Qlik to Power BI Equivalents

| Qlik Concept | Power BI Equivalent |
|---|---|
| Set Analysis | DAX CALCULATE + FILTER |
| Master Items | DAX Measures |
| Straight Table | Table / Matrix Visual |
| Bar Chart | Clustered Bar Chart |
| KPI Object | Card Visual |
| Bookmarks | Power BI Bookmarks |
| Variables | What-If Parameters |

### Step 3 — Rebuild in Power BI
- Recreate data model in Power BI
- Write DAX measures to match Qlik calculations
- Design visuals to match original layout
- Add dynamic slicers and drillthrough pages

### Step 4 — Validate & Reconcile
- Compare every number between Qlik and Power BI
- Run SQL queries to verify both match source data
- Fix any discrepancies in DAX measures
- Document all validation results

### Step 5 — Stakeholder Signoff
- Demo new Power BI dashboard to stakeholders
- Collect feedback and make adjustments
- Get formal signoff before retiring Qlik version
- Train users on new Power BI features

---

## 💡 Key Learnings

### ✅ What Worked Well
- Breaking migration into small batches (2-3 dashboards at a time)
- Running Qlik and Power BI in parallel during validation
- Using SQL as the single source of truth for reconciliation
- Weekly sync with stakeholders to show progress

### ⚠️ Challenges Faced
- Qlik Set Analysis is complex to replicate in DAX
- Some Qlik visuals have no direct Power BI equivalent
- Performance tuning needed for large data models
- User training required for new Power BI interface

---

## 📈 Results Achieved

| Metric | Before (Qlik) | After (Power BI) | Improvement |
|---|---|---|---|
| Report Refresh Time | 2 hours | 72 minutes | ⬇️ 40% faster |
| Manual Steps | 15 steps | 4 steps | ⬇️ 73% reduction |
| Automation Rate | 45% | 80% | ⬆️ 35% increase |
| Stakeholder Satisfaction | 3.2/5 | 4.6/5 | ⬆️ 44% increase |

---

## 🤝 Connect with Me
- 💼 [LinkedIn](https://linkedin.com/in/sadhana-s-kumar)
- 📧 sanasadhana07@gmail.com
- 🐙 [GitHub Profile](https://github.com/sadhana007)
