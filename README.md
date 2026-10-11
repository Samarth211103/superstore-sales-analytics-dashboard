# Superstore Sales Analytics Dashboard

An end-to-end retail analytics project on the Superstore dataset: raw data cleaning and pivot analysis in Excel, followed by a 6-page interactive Power BI dashboard covering sales, profit, regional and manager performance, targets, YoY growth, returns and shipping delays.

---

## Repository Contents

| File | Description |
|------|-------------|
| `SUPERSTORE_GLOBAL_SALES_DASHBOARD.pbix` | Power BI report (6 pages, DAX measures, data model) |
| `Cleaned_and_Analysed_Superstore_Dataset.xlsx` | Cleaned dataset (`Sample - Superstore`) + pivot analysis (`Pivot Analysis`) |
| `Raw_Superstore_Dataset.csv` | Original uncleaned data, kept for reproducibility |

Suggested layout:

```
superstore-sales-analytics-dashboard/
├── README.md
├── data/
│   ├── Raw_Superstore_Dataset.csv
│   └── Cleaned_and_Analysed_Superstore_Dataset.xlsx
└── dashboard/
    └── SUPERSTORE_GLOBAL_SALES_DASHBOARD.pbix
```

---

## Dataset Overview

- **Rows:** 9,994 order lines | **Orders:** 5,009 | **Customers:** 793
- **Period:** 2014 – 2017
- **Geography:** United States (4 regions: Central, East, South, West)
- **Hierarchy:** 3 categories (Furniture, Office Supplies, Technology) → 17 sub-categories
- **Segments:** Consumer, Corporate, Home Office
- **Key fields:** Order/Ship Date, Ship Mode, Customer, Segment, City/State/Region, Product, Sales, Quantity, Discount, Profit, Profit Margin

The Power BI model also brings in returns, regional manager and sales target data to power the return-rate, manager and target-vs-actual visuals.

---

## Dashboard Pages

1. **Executive Overview** – KPI cards (Total Sales, Total Profit, Total Orders, Profit Margin %, Return Rate %, Delay Rate %), sales vs profit by year, sales vs target trend, regional sales share. Slicers for Category, Year and Region.
2. **Region Performance** – Sales treemap, profit margin by region, returns and delayed orders by region, yearly sales mix, city-level profit map.
3. **Manager Performance** – Sales vs profit and sales vs target per regional manager, returns vs margin scatter, delays and return counts, margin ranking.
4. **Category vs Target** – Sales against target by category (gauge, combo and line charts), sales-gap waterfall, year × category pivot.
5. **YoY Analysis** – YoY sales growth by category and region, profit trends by region, sales and profit over time, margin KPI.
6. **Returns & Delays** – Returns by ship mode, return rate by sub-category, delayed orders by ship mode, region × category return breakdown.

---

## Headline Findings

| Metric | Value |
|--------|-------|
| Total Sales | ~$2.30M |
| Total Profit | ~$286K |
| Overall Profit Margin | ~12.5% |
| Sales growth 2014 → 2017 | ~$484K → ~$733K (+51%) |
| Best category by profit | Technology (~$145K) |
| Weakest category | Furniture: ~$742K sales but only ~$18K profit (~2.5% margin) |
| Best region by profit | West (~$108K) |
| Weakest region | Central (~$40K profit on ~$501K sales) |
| Loss-making sub-categories | Tables (~-$17.7K), Bookcases, Supplies |
| Loss-making states | Texas (~-$25.7K), Ohio (~-$17.0K) |
| Seasonality | Sales rise every quarter; Q4 is the strongest (~$878K vs ~$360K in Q1, all years combined) |

> Figures calculated from the cleaned dataset. Dashboard values will change with slicer selections.

---

## Workflow

1. **Data cleaning (Excel)** – Removed stray/helper columns from the raw export, fixed date types, and added a `Profit Margin` field.
2. **Exploratory analysis (Excel)** – Pivot tables for sales by quarter, category and sub-category, top profit by city and region, and sales quartiles.
3. **Data modelling (Power BI)** – Loaded the cleaned data and supporting tables, built relationships and a date dimension.
4. **DAX measures** – Total Sales, Total Profit, Total Orders, Profit Margin %, Return Rate %, Delay Rate %, Sales Target, Sales Gap, YoY Sales Growth %.
5. **Visualisation** – Six themed report pages with cross-filtering slicers.

---

## Tools Used

- **Microsoft Excel** – data cleaning, pivot tables
- **Power BI Desktop** – data modelling, DAX, dashboarding

---

## How to Use

1. Clone or download this repository.
2. Open `SUPERSTORE_GLOBAL_SALES_DASHBOARD.pbix` in **Power BI Desktop** (the file embeds its data, so it opens ready to explore).
3. To refresh from source, point the data source to `data/Cleaned_and_Analysed_Superstore_Dataset.xlsx` via *Transform data → Data source settings*.

---

## Recommended Actions (from the analysis)

- Review pricing and discounting on **Tables** and **Bookcases**, the main drag on Furniture margin.
- Investigate loss-making states (**Texas, Ohio**) for discount depth and shipping costs.
- Prioritise Technology and Office Supplies, which drive most profit.
- Plan inventory and staffing around the strong **Q4** peak.
- Reduce delayed orders and returns in the worst-performing ship modes and sub-categories.

---

## Author

**Samarth Gupta**
B.Tech in Computer Science | Aspiring Data Analyst
[LinkedIn](https://www.linkedin.com/in/your-profile) · [GitHub](https://github.com/your-username) · [Portfolio](https://your-portfolio-link)

---

## Acknowledgements

Based on the publicly available Superstore sales dataset, used here for learning and portfolio purposes.
