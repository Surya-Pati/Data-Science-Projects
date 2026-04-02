# Sales & Profit Analytics Dashboard
 
This project delivers a two-view interactive Excel dashboard to analyze sales performance, profitability, discount impact, customer segments, and regional trends across a Superstore dataset. The objective is to provide business stakeholders with clear, actionable insights for decision-making and operational improvement.
 
---
 
## Project Overview
 
The Superstore dataset contains 9,993 transactional sales records spanning 2014–2017 across three product categories, four regions, and three customer segments. By leveraging Excel's advanced features — PivotTables, combo charts, scatter plots, waterfall charts, and slicers connected via Report Connections — this dashboard enables dynamic exploration of KPIs and supports business intelligence reporting across two analytical lenses: **Category & Sub-Category Analysis** and **Region & Segment Analysis**.
 
---
 
## Objectives
 
- Build a multi-view Excel dashboard to visualize sales, profitability, and discount trends
- Identify loss-making sub-categories and underperforming regions by profit margin
- Quantify the impact of discounting on profit margin using scatter analysis
- Segment performance by product category, customer type, and region
- Provide interactive filters for dynamic, stakeholder-ready analysis
- Support business reporting and operational decision-making
 
---
 
## Dataset
 
- **Source:** Superstore dataset (publicly available)
- **Size:** 9,993 orders · 2014–2017 · United States
- **Features:** Order ID, product category, sub-category, sales, profit, discount, profit margin, customer segment, region, ship mode, and order/ship dates
- **Target:** Business insights through dashboard visualization
 
---
 
## Key Business Findings
 
### Profitability
- **Technology** is the highest-revenue category at ₹8,36,221 with a 17.39% profit margin
- **Furniture** generates ₹7,41,725 in revenue but delivers only a **2.49% profit margin** — the lowest of all categories despite being the second-highest seller
- **Office Supplies** achieves a strong 17.03% margin on ₹7,19,127 in sales
 
### Loss-Making Sub-Categories
Three sub-categories are actively destroying value:
 
| Sub-Category | Sales | Profit | Margin |
|---|---|---|---|
| Tables | ₹2,06,968 | -₹17,733 | -8.57% |
| Bookcases | ₹1,14,879 | -₹3,479 | -3.03% |
| Supplies | ₹46,679 | -₹1,187 | -2.54% |
 
### Discount Impact
- Discount correlates with profit margin at **-0.86** — a near-perfect negative relationship
- Orders at 40%+ discount collectively generated a **loss of ₹1,22,632** across 1,113 orders
- The scatter plot on Dashboard 1 visualizes this trend with a trendline showing the steep profitability cliff beyond 20% discount
 
### Regional Performance
- **West** leads in both sales (₹7,25,514) and profit margin (14.94%)
- **Central** region is the weakest performer at a 7.92% profit margin — nearly half of West
- Central's Furniture sub-category is loss-making at -1.75% margin, indicating a product-mix problem rather than a market problem
 
### Segment Insights
- **Consumer** segment drives the highest revenue contribution at ₹11,61,497
- All three segments show consistent profit growth from 2014 to 2017
- **Corporate** segment demonstrates the steepest profitability improvement across quarters
 
---
 
## Methodology
 
1. **Data Preparation**
   - Cleaning and formatting raw transactional data across 26 columns
   - Engineering calculated fields: Profit Margin, Profit Ratio, Quarter, Order Month (YYYY-MM)
   - Structuring data as an Excel Table for dynamic slicer connectivity
 
2. **Dashboard Architecture**
   - PivotTables as the data source for all charts, enabling slicer control via Report Connections
   - Single slicer set (Segment, Category, Region, Order Date) controls all charts across both dashboard views simultaneously
   - Two dashboard tabs — Category & Sub-Category Analysis and Region & Segment Analysis — for focused stakeholder views
 
3. **Charts & Visuals**
   - **KPI cards** — Total Sales, Total Profit Margin %, Total Orders, Total Profit (top of both dashboards)
   - **Waterfall/bar chart** — Sub-category profit showing loss-making lines in negative (Tables, Bookcases, Supplies)
   - **Column chart** — Category sales,Profit and profit margin % trends visualized
   - **Scatter plot** — Discount % vs Profit Margin % with trendline showing -0.86 correlation
   - **Region margin chart** — Sales bars with profit margin % labels per region
   - **Profitability across segments** — Line chart tracking segment profit growth quarterly 2014–2017
   - **Monthly sales trend** — Line chart showing revenue seasonality across full date range
   - **Segment contribution** — Donut chart showing revenue share by customer type
 
4. **Insights**
   - Identification of high-performing and loss-making categories and sub-categories by profit margin
   - Discount impact analysis with quantified revenue and profit loss from excessive discounting
   - Regional profitability benchmarking to guide resource allocation decisions
   - Segment-level profitability trends for targeted marketing and retention strategies
 
---
 
## Results
 
- Furniture identified as a **high-revenue, low-margin risk** — expansion recommended only in South and West regions where margins are positive (5.77% and 4.55% respectively)
- Tables sub-category flagged for **immediate discount review** — currently losing ₹17,733 despite ₹2L+ in sales
- Discount cap recommendation: **orders above 20% discount** account for the majority of loss-making transactions
- Central region underperformance traced to Furniture product mix, not overall market weakness
- Dashboard enables any stakeholder to filter by segment, category, region, or time period and immediately see the profitability impact
 
---
 
## Technologies Used
 
- Microsoft Excel
- PivotTables with Report Connections for unified slicer control
- Combo charts, scatter plots, waterfall charts, donut charts, line charts
- Conditional formatting for loss/profit color encoding
- Data cleaning, KPI calculation, and profit margin engineering
 
---
 
## How to Run
 
- Open the file:
  `Superstore_Dataset_Insights_Dashboard.xlsx`
- Navigate to **Dashboard 1** (Category & Sub-Category Analysis) or **Dashboard 2** (Region & Segment Analysis)
- Use the slicers on the left — **Segment**, **Category**, **Region**, and **Order Date** — to filter all charts simultaneously
- KPI cards at the top update dynamically to reflect the current filter selection
 
---
 
## Purpose
 
This project demonstrates capabilities in:
 
- Multi-view dashboard creation and business intelligence reporting using Excel
- Profit margin analysis and loss identification across product categories and regions
- Discount impact quantification using correlation analysis and scatter visualization
- PivotTable architecture with Report Connections for scalable, slicer-driven dashboards
- Translating raw transactional data into stakeholder-ready, decision-driving insights
 
---
 
## Acknowledgements
 
Thanks to the Superstore dataset providers, open-source resources, and the data science community for enabling this analysis.
 
