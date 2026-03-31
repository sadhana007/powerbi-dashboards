# 📊 DAX Measures — KPI Tracking

> Author: Sadhana S Kumar
> Tools: Power BI, DAX
> Description: Core DAX measures used in enterprise dashboards

---

## 💰 Revenue Measures
```dax
-- Total Revenue
Total Revenue = 
SUMX(fact_transactions, [revenue])

-- Total Revenue Last Month
Total Revenue LM = 
CALCULATE(
    [Total Revenue],
    PREVIOUSMONTH(dim_date[date])
)

-- Month over Month Revenue Growth
MoM Revenue Growth % = 
DIVIDE(
    [Total Revenue] - [Total Revenue LM],
    [Total Revenue LM],
    0
) * 100

-- Year to Date Revenue
YTD Revenue = 
TOTALYTD([Total Revenue], dim_date[date])

-- Quarter to Date Revenue
QTD Revenue = 
TOTALQTD([Total Revenue], dim_date[date])
```

---

## 📈 Product Adoption Measures
```dax
-- Monthly Active Users
MAU = 
DISTINCTCOUNT(fact_user_activity[user_id])

-- MAU Last Month
MAU LM = 
CALCULATE(
    [MAU],
    PREVIOUSMONTH(dim_date[date])
)

-- MAU Growth %
MAU Growth % = 
DIVIDE(
    [MAU] - [MAU LM],
    [MAU LM],
    0
) * 100

-- Feature Adoption Rate
Feature Adoption Rate % = 
DIVIDE(
    DISTINCTCOUNT(fact_feature_usage[user_id]),
    DISTINCTCOUNT(dim_users[user_id]),
    0
) * 100
```

---

## ⚙️ Operational KPI Measures
```dax
-- Average Processing Time (minutes)
Avg Processing Time = 
AVERAGE(fact_orders[processing_time_minutes])

-- Order Completion Rate
Completion Rate % = 
DIVIDE(
    CALCULATE(
        COUNT(fact_orders[order_id]),
        fact_orders[status] = "completed"
    ),
    COUNT(fact_orders[order_id]),
    0
) * 100

-- Automation Efficiency Score
Automation Efficiency % = 
DIVIDE(
    CALCULATE(
        COUNT(fact_orders[order_id]),
        fact_orders[is_automated] = TRUE()
    ),
    COUNT(fact_orders[order_id]),
    0
) * 100
```

---

## 🔄 Rolling Averages
```dax
-- Rolling 3 Month Average Revenue
Rolling 3M Avg Revenue = 
CALCULATE(
    AVERAGE(fact_transactions[revenue]),
    DATESINPERIOD(
        dim_date[date],
        LASTDATE(dim_date[date]),
        -3,
        MONTH
    )
)

-- Rolling 12 Month Average Revenue
Rolling 12M Avg Revenue = 
CALCULATE(
    AVERAGE(fact_transactions[revenue]),
    DATESINPERIOD(
        dim_date[date],
        LASTDATE(dim_date[date]),
        -12,
        MONTH
    )
)
```

---

## 🎯 Dynamic KPI Indicators
```dax
-- Revenue Status Indicator
Revenue Status = 
SWITCH(
    TRUE(),
    [MoM Revenue Growth %] >= 10, "🟢 Strong Growth",
    [MoM Revenue Growth %] >= 0,  "🟡 Stable",
    [MoM Revenue Growth %] < 0,   "🔴 Declining"
)

-- Completion Rate Status
Completion Status = 
SWITCH(
    TRUE(),
    [Completion Rate %] >= 95, "🟢 Excellent",
    [Completion Rate %] >= 80, "🟡 Good",
    [Completion Rate %] < 80,  "🔴 Needs Attention"
)
```
