# Task 1 — Business Sales Dashboard (E‑commerce)

**Goal:** Identify best-selling products, sales trends, and revenue-driving categories.

## Dataset
`data/ecommerce_sales.csv` with columns:
- OrderID, OrderDate, Category, Subcategory, Product, Region, Quantity, UnitPrice, UnitCost, Sales

## Steps (Excel/Power BI)
1) Import the CSV.
2) Clean: set `OrderDate` to Date, check duplicates.
3) Create measures (Power BI DAX):
   - **Total Sales** = SUM(Sales)
   - **Total Quantity** = SUM(Quantity)
   - **Total Profit** = SUMX(ALL('Table'), 'Table'[Quantity] * ('Table'[UnitPrice] - 'Table'[UnitCost]))
4) Build visuals:
   - Line: Sales by Month (use `OrderDate`)
   - Bar: Top 10 Products by Sales
   - Bar: Category-wise Sales / Profit
   - Map (optional): Sales by Region
5) Insights: Summarize 3–5 bullet points (seasonality, top categories, regions).

## Deliverables
- Dashboard (PBIX / screenshots if using Excel)
- `insights.md` with key findings
- `README.md` (this file)

## Screenshot ideas
- KPI cards: Total Sales, Profit, Avg Order Value
- Trend chart: Monthly Sales
- Composition: Sales by Category
