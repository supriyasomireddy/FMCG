# FMCG-Analytics

## Project Overview  
This Power BI dashboard delivers **actionable, data-driven insights** for an FMCG business, enabling stakeholders to monitor sales performance, customer behavior, product trends, and time-based KPIs across regions and categories. Built with a clean, interactive design, it supports strategic decision-making in a competitive retail and distribution environment.

The dashboard consolidates data from **Sales, Products, Customers, Date, and Geography** tables into a semantic model, leveraging **DAX measures**, **dynamic visuals**, and **smart filtering** for intuitive exploration.

---

## Dashboard Preview – Report Pages  

This Power BI solution consists of **four interactive report pages**, each designed with a specific analytical purpose.  
The images below provide a visual preview of every page in the dashboard.

> 🔹 Replace the image paths below with the actual GitHub paths after uploading your screenshots.

---

### 🏠 1. Homepage  

![Homepage Preview](/HOME%20PAGE.jpeg)

The **Homepage** serves as the navigation hub of the report — giving users access to  
Sales Analysis, Customer Insights, and the Information page in a clean and intuitive layout.

---

### 📊 2. Sales Analysis Page  

![Sales Analysis Preview](/SALES%20ANALYSIS%20PAGE.jpeg)

The **Sales Analysis Page** focuses on business performance metrics such as  
sales contribution, time-based performance (MTD/QTD/YTD), product trends,  
regional distribution, and monthly movement using KPI visuals and trend charts.

---

### 👥 3. Customer Analysis Page  

![Customer Analysis Preview](/CUSTOMER%20ANALYSIS%20PAGE.jpeg)

The **Customer Analysis Page** highlights engagement, loyalty segmentation,  
regional distribution, top & bottom performing customers, and transaction trends —  
helping stakeholders understand customer behavior and performance patterns.

---

### ℹ️ 4. Info Page  

![Info Page Preview](/INFO%20PAGE.jpeg)

The **Info Page** documents key report details including the data model approach,  
data sources used, DAX calculations, RLS configuration, navigation guidance,  
and performance optimization practices followed during development.

---


## Tools Used  
- **Excel** – Primary data source and initial exploration  
- **Power BI Desktop** – Data modeling, DAX, visualization, and report design  
- **DAX (Data Analysis Expressions)** – Core calculations and time intelligence  
- **Power Query (M Language)** – Data transformation, cleaning, and date table creation  

---

## Power BI Techniques Implemented  

| Technique | Usage |
|--------|-------|
| **Calculated Measures (DAX)** | Dynamic KPIs like MTD/QTD/YTD, YoY Growth, Last 3 Months Sales |
| **Time Intelligence** | `DATESMTD`, `DATESQTD`, `DATESYTD`, `SAMEPERIODLASTYEAR`, `DATESINPERIOD` |
| **Disconnected Slicer Table** | Unified Time Period slicer (MTD/QTD/YTD/Last 3 Months) using `SWITCH` |
| **Conditional Formatting** | Growth % (green/red), table icons, gauge targets |
| **Slicers & Cross-Filtering** | Region, Product Category, Loyalty Status, Date Range |
| **Responsive Layout** | Optimized for desktop and mobile (Fit to Page) |
| **Row-Level Security (Static & Dynamic)** | Region-based secure access and user-email driven dynamic filtering |
| **Bookmarks & Tooltip Reports** | Interactive toggle between Top/Bottom customers and quarter-wise tooltips |

---

## Dashboard Structure  

### 1. **Executive Summary**  
- **KPI Cards**: Total Sales, YoY Growth, CLV, Inventory Turnover  
- **Line Chart**: Sales Trend Over Time  
- **Gauge**: Current vs. Target Sales  

---

### 2. **Sales Analysis**  
- **Clustered Column**: Sales by Category & Region  
- **Top 10 Products Bar Chart**  
- **YoY Growth Area Chart**  
- **Detailed Sales Matrix**  

- **Top & Bottom Customer Insights using Bookmarks**  
  - Top 5 Customers by Quantity Purchased  
  - Top 5 Customers by Sales Value  
  - Bottom 5 Customers by Quantity Purchased  
  - Bottom 5 Customers by Sales Value  

Users can **switch between Top 5 and Bottom 5 visuals using bookmark-based toggle buttons**, reducing clutter while improving insight clarity.

---

### 3. **Customer Analysis**  
- **Donut**: Loyalty Status Distribution  
- **Scatter**: Spend vs. Visit Frequency  
- **Stacked Bar**: New vs. Returning Customers  
- **Customer Segmentation Matrix**  

- **Spotter System (Performance Tracking)**  
  Identifies customers whose performance is **increasing or decreasing**, helping business users quickly detect growth or risk signals.

---

### *(Optional)* **Branch Performance**  
- **Map Visual**: Revenue by Location  
- **Branch Sales KPIs**  

---

## Tooltip Analytics (Quarter-Wise Customer Trends)

Custom **tooltip pages** were designed to display **quarterly purchase trends per customer** when hovering over:

- Top 5 (Quantity & Sales)  
- Bottom 5 (Quantity & Sales)  

This provides **context-aware insights without navigating to another page**.

---

## Domain Knowledge (FMCG Context)  

| Area | Key Concepts Covered |
|------|------------------------|
| **Sales** | Regional performance, category contribution, top SKUs |
| **Customer** | Loyalty tiers, acquisition vs. retention, lifetime value |
| **Product** | Inventory turnover, fast vs. slow movers |
| **Time Analysis** | MTD/QTD/YTD, rolling 3-month trends, YoY comparison |

---

## Business Terms Used  

- **MTD / QTD / YTD** – Month/Quarter/Year to Date  
- **YoY Growth** – Year-over-Year percentage change  
- **Customer Lifetime Value (CLV)** – Total spend per customer  
- **Inventory Turnover** – Sales efficiency relative to stock  
- **New vs. Returning Customers** – Acquisition & retention tracking  

---

## Row-Level Security (Static & Dynamic)

### **Static RLS**  
Region-based restriction so users only see data belonging to their assigned region.

### **Dynamic RLS**  
Implemented using **USERPRINCIPALNAME()**, ensuring **email-driven automatic security filtering**.

This guarantees **secure, role-appropriate access control** across all regions.

---

## Company’s Background: NovaMart Consumer Goods  
**NovaMart Consumer Goods** is a fast-growing FMCG company operating in the packaged food, personal care, and household essentials space. With a strong presence across urban and semi-urban markets in multiple regions, NovaMart distributes its products through modern trade (supermarkets), general trade (kirana stores), and e-commerce platforms. Facing increasing competition and margin pressure, the company is leveraging data analytics for the first time to optimize inventory, boost customer retention, and drive sales efficiency across channels.

---

## Importing Data into Power BI  
Data is sourced from **Excel workbooks** containing structured tables:  
`Sales`, `Products`, `Customers`, `Date`, `Geography`  

All files are imported via **Power Query**, transformed, and

## Importing Data into Power BI  
Data is sourced from **Excel workbooks** containing structured tables:  
`Sales`, `Products`, `Customers`, `Date`, `Geography`  

All files are imported via **Power Query**, transformed, and loaded into the model.  

**Relationships established via**:  
- `Sales[ProductID]` → `Products[ProductID]`  
- `Sales[CustomerID]` → `Customers[CustomerID]`  
- `Sales[Date]` → `Date[Date]`  
- `Sales[RegionID]` → `Geography[RegionID]`  

---

## Dashboard Navigation  

- **Slicers**:  
  - Region  
  - Category  
  - Loyalty  
  - Unified Time Period  

- **Bookmarks**:  
  - Drill to product details  
  - Reset filters  
  - Toggle between **Top 5 and Bottom 5 customer insights**  

---

**Ready to deploy?**  
**Publish to Power BI Service** → **Create App** → **Share with stakeholders.**
