# Online Retail Sales Analysis
Portfolio Project | Excel Data Analysis

## Background
End-to-end analysis of real UK e-commerce sales data: cleaning messy raw data, building advanced formulas, and turning numbers into business insights.

## Data Source
**Online Retail II** (Kaggle) — ~542,000 order records from a UK online store, Jan 2010–Dec 2011.

## Process

### 1. Data Cleaning
- **135,080 rows** missing Customer ID — removed
- **9,288 cancellation rows** (Invoice starting with "C") — moved to a separate Returns sheet
- **2,517 rows** with zero/negative price — removed as bad data
- **5,268 duplicates** — removed
- Fixed inconsistent date formats (two formats in the raw file) and converted to real dates

**Result:** ~390,000 clean rows from 541,910 original (note: ~25% removed, mostly due to missing Customer ID — affects customer-level analysis only, not overall sales analysis).

### 2. Calculated Columns
- **Revenue** (Quantity × Price)
- **InvoiceMonth** (for trend analysis)

### 3. RFM Analysis
Scored 4,338 unique customers using MAXIFS, SUMIF, and PERCENTRANK, then split into 4 segments: VIP, Active, At Risk, Churned.

**Key finding:** ~25% of customers (1,100 of 4,338) are Churned.

### 4. Pivot Tables & Dashboard
4 pivot tables (revenue by month, by country, top products, customer segments) combined into one Dashboard with charts.

## Key Insights
- **Seasonal growth** — sales peaked Sep–Nov 2011, likely holiday season
- **High churn** — 25% of customers at risk/churned, needs retention focus
- **Single-market dependency** — UK dominates revenue, room for international growth
- **Category focus** — top products are all home décor/gifts, volume-based model

## Tools & Functions
`SUMIF` `MAXIFS` `PERCENTRANK.INC` `IFS` `TEXT` `TRIM` `Pivot Tables` `Excel Tables` `Data Visualization`

## File Structure
| Sheet | Content |
|---|---|
| Clean Data | Cleaned dataset |
| Returns | Cancellations/returns |
| RFM | Full customer analysis |
| Month/Country/Products Pivot | Pivot tables |
| Dashboard | Visual summary |
| Insights | Business findings & recommendations |
