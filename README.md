# 🏪 Retail Performance Analysis & Business Intelligence Dashboard
### Project #1 · Data Analyst Portfolio · Hugo Ernesto Aguilar Gallardo

---

<div align="center">

![Excel](https://img.shields.io/badge/Excel-Advanced-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL%20Pipeline-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-Business%20Queries-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-00C853?style=for-the-badge)

</div>

---

## 📋 Project Overview · Descripción del Proyecto

**EN** · End-to-end retail business analysis using a custom-built dataset. Starting from a raw, messy dataset, the project covers the full data analyst pipeline: data cleaning, transformation via Power Query, exploratory analysis with Pivot Tables, profitability analysis by category and region, and a final strategic action plan with prioritized business recommendations.

**ES** · Análisis completo de negocio retail usando un dataset construido desde cero. Partiendo de datos crudos y desordenados, el proyecto cubre el pipeline completo de un analista de datos: limpieza, transformación con Power Query, análisis exploratorio con Tablas Dinámicas, análisis de rentabilidad por categoría y región, y un plan de acción estratégico con recomendaciones priorizadas de negocio.

---

## 🎯 Business Questions · Preguntas de Negocio

> *What is actually driving revenue — and what is silently killing profitability?*
> *¿Qué está generando revenue real — y qué está destruyendo silenciosamente la rentabilidad?*

| # | Business Question | Answer Found |
|---|-------------------|--------------|
| 1 | Which product category generates the most revenue? | ✅ Technology ($30,260 total — 75% of revenue) |
| 2 | Which categories are profitable vs unprofitable? | ✅ Technology & Furniture: deeply negative margins |
| 3 | Which region underperforms significantly? | ✅ East region ($270 total vs $14K in Central) |
| 4 | Which sub-categories should be prioritized or cut? | ✅ Cut Phones & Copiers · Promote Binders & Paper |
| 5 | What are the top strategic actions for the business? | ✅ 5-priority action plan delivered |

---

## 🗂️ Dataset Structure · Estructura del Dataset

| Field | Description |
|-------|-------------|
| `Order_ID` | Unique transaction identifier |
| `Order Date / Ship Date` | Transaction and delivery timestamps |
| `Ship_Mode` | Shipping method (Second Class, First Class, etc.) |
| `Customer_ID / Customer Name` | Customer identifiers |
| `Segment` | Customer segment (Consumer, Corporate, Home Office) |
| `Region / State / City` | Geographic breakdown |
| `Category / Sub-Category` | Product classification |
| `Product Name` | Full product description |
| `Sales` | Revenue per transaction |
| `Quantity` | Units sold |
| `Discount` | Applied discount rate |
| `Profit` | Net profit per transaction |

**Dataset:** 46 transactions · 20 columns · United States market · FY 2023

---

## 🔧 Technical Process · Proceso Técnico

### Phase 1 · Data Cleaning & ETL
```
Raw messy dataset → Power Query transformation → Clean structured dataset
```
- Standardized column naming conventions (`Order_ID`, `customer_id`, `Product_ID`)
- Fixed data types: Sales, Profit, Discount converted from text to numeric
- Removed formatting inconsistencies across date fields
- Built reusable Power Query pipeline for future data refreshes

### Phase 2 · Formula Practice & Lookup Logic
```excel
VLOOKUP  →  =VLOOKUP(A2, 'Raw_Data'!$A$2:$O$50, 14, 0)
INDEX-MATCH  →  =INDEX('Raw_Data'!$N$2:$N$50, MATCH(A2, 'Raw_Data'!$A$2:$A$50, 0))
IFERROR  →  =IFERROR(VLOOKUP(...),"Not Found")
```
- Applied VLOOKUP for category and sales lookups
- Used INDEX-MATCH for flexible two-way lookups
- Wrapped with IFERROR for clean error handling

### Phase 3 · Pivot Table Analysis
Three pivot tables built to answer specific business questions:

| Pivot Table | Purpose |
|-------------|---------|
| `PT_Sales_by_Category` | Revenue breakdown by product category |
| `PT_Sales_by_Region_Category` | Cross-analysis: region × category performance |
| `PT_Profitability_Analysis` | Margin analysis: sales vs profit by sub-category |

### Phase 4 · Business Insights & Action Plan
Strategic recommendations delivered with priority classification.

---

## 📊 Key Findings · Hallazgos Clave

### Revenue by Category
| Category | Total Sales | % of Revenue |
|----------|-------------|--------------|
| 🖥️ Technology | $22,805 | 75.4% |
| 🪑 Furniture | $5,508 | 18.2% |
| 📎 Office Supplies | $1,947 | 6.4% |
| **Total** | **$30,260** | **100%** |

### ⚠️ Profitability Crisis — The Hidden Problem
> Technology leads revenue but has a **-66.9% profit margin**. The business is generating losses on its best-selling category.

| Sub-Category | Sales | Profit | Margin |
|--------------|-------|--------|--------|
| 📱 Phones | $8,967 | -$7,631 | **-85.1%** |
| 🖨️ Copiers | $11,200 | -$8,400 | **-75.0%** |
| 🏠 Appliances | $823 | -$937 | **-113.9%** |
| ✅ Machines | $2,500 | +$750 | **+30.0%** |
| ✅ Binders | $532 | +$173 | **+32.6%** |
| ✅ Paper | $65 | +$22 | **+33.8%** |

### Regional Performance
| Region | Total Sales | Status |
|--------|-------------|--------|
| Central | $13,999 | ✅ Main market |
| West | $11,682 | ✅ Strong |
| South | $4,309 | ⚠️ Moderate |
| East | $270 | 🔴 Critical underperformance |

---

## 🚨 Strategic Action Plan · Plan de Acción Estratégico

| Priority | Area | Recommended Action |
|----------|------|-------------------|
| 🔴 CRITICAL | Technology | **Stop Phones sales immediately** and renegotiate Copiers contracts |
| 🟠 HIGH | Furniture | Review pricing strategy on Tables & Chairs · Promote Bookcases (only profitable line) |
| 🟡 MEDIUM | Region | Merge or close East region ($270 total) with Central to reduce operating costs |
| 🔵 OPERATIONAL | Product Mix | Eliminate Appliances (-113% margin) · Promote Paper & Fasteners (high profitability) |
| ⚪ NEXT STEP | Audit | Full cost breakdown by supplier · Audit discount policies in last quarter |

---

## 💡 Business Impact · Impacto de Negocio

**EN** · This analysis reveals a critical disconnect between revenue and profitability. The company's top-selling category (Technology) is its most unprofitable, generating **-$15,257 in losses** on $22,805 in revenue. Without intervention, growth in Technology sales accelerates losses. The action plan prioritizes immediate revenue protection and margin recovery.

**ES** · Este análisis revela una desconexión crítica entre revenue y rentabilidad. La categoría más vendida (Technology) es la más deficitaria, generando **-$15,257 en pérdidas** sobre $22,805 de revenue. Sin intervención, el crecimiento en ventas de Technology acelera las pérdidas. El plan de acción prioriza la protección inmediata del revenue y la recuperación de márgenes.

---

## 📁 Repository Structure · Estructura del Repositorio

```
📦 Retail-Performance-Analysis/
├── 📊 Real_Business_Cases_MASTER.xlsx   # Main workbook
│   ├── retail_sales_messy_dataset       # Original raw data
│   ├── Raw_Data                         # Cleaned structured data
│   ├── PT_Sales_by_Category             # Pivot: revenue by category
│   ├── PT_Sales_by_Region_Category      # Pivot: region × category
│   ├── PT_Profitability_Analysis        # Pivot: margin analysis
│   ├── Action_Plan                      # Strategic recommendations
│   └── Practice_formulas               # VLOOKUP · INDEX-MATCH · IFERROR
└── 📄 README.md                         # This document
```

---

## 🛠️ Skills Demonstrated · Habilidades Demostradas

- ✅ **Data Cleaning** — Identifying and fixing data type issues, naming inconsistencies
- ✅ **Power Query** — ETL pipeline for repeatable data transformation
- ✅ **Excel Formulas** — VLOOKUP, INDEX-MATCH, IFERROR in real business context
- ✅ **Pivot Tables** — Multi-dimensional analysis: category, region, profitability
- ✅ **Business Thinking** — Translating data findings into prioritized strategic actions
- ✅ **Data Storytelling** — Communicating insights for non-technical decision makers

---

## 👤 Author · Autor

**Hugo Ernesto Aguilar Gallardo**
Data Analyst | Marketing & Business Intelligence · Ciudad de México 🇲🇽

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/ernesto-aguilar-gallardo-2359263a5)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=flat-square&logo=gmail)](mailto:ernestoaguiga@gmail.com)
[![Portfolio](https://img.shields.io/badge/GitHub-Portfolio-181717?style=flat-square&logo=github)](https://github.com/Ernestoaguiga)

---

<div align="center">

*Data that speaks. Visuals that sell. Business that grows.*

</div>
