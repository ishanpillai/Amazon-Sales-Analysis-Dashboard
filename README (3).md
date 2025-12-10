# 📊 Amazon Sales Analysis Dashboard – Power BI

A comprehensive Power BI sales analytics dashboard showcasing performance trends, category insights, and product-level metrics using Amazon e-commerce data.

## 🚀 Project Overview
This dashboard provides a 360° view of Amazon’s sales performance with interactive visuals, custom KPIs, and a clean UI theme.

It helps stakeholders quickly understand:
- Overall YTD & QTD performance
- Monthly & weekly sales trends
- Category-level contributions
- Top-performing products
- Customer engagement through reviews

## 🎯 Key Highlights

### Performance KPIs
- YTD Sales
- QTD Sales
- YTD Products Sold
- YTD Customer Reviews

## 📈 Trend Analysis

### Sales by Month (Line Chart)
- Shows monthly fluctuations, growth patterns, and seasonal spikes.

### Sales by Week (Bar Chart)
- Reveals weekly demand cycles and operational trends.

## 🧩 Category-Level Insights
- YTD Sales
- QTD Sales
- % Contribution to Total Sales
- All Product Categories (Accessories, Clothing, Camera, Toys, etc.)

## 🏆 Top Product Insights
- Top 5 Products by YTD Sales
- Top 5 Products by YTD Reviews

## 🎛️ Interactive Slicers
- Product Category Filter
- Quarter Filter

## 📁 Dataset Structure

### Amazon_Data (Fact Table)
- Order Date
- Price
- Product Category
- Product Description
- Number of Reviews
- Units Sold (inferred)

### Date Table (Dimension)
- Date
- Month
- Month Number
- Quarter
- Week Number

## 🧠 Business Problems Solved
- How are sales performing YTD?
- Which months or weeks show peak demand?
- Which categories drive revenue?
- What products are trending based on sales and reviews?
- Are specific categories excelling in certain quarters?

## 🔧 Power BI Features Used
- Custom KPI cards
- Time intelligence calculations (YTD, QTD)
- Line, bar, and matrix visuals
- Bookmarks & slicers
- Star schema modeling
- Custom theme

## 🧮 DAX Calculations

```DAX
YTD Sales =
TOTALYTD(SUM(Amazon_Data[Price]), 'Date Table'[Date])

QTD Sales =
TOTALQTD(SUM(Amazon_Data[Price]), 'Date Table'[Date])

YTD Products Sold =
TOTALYTD(SUM(Amazon_Data[Units Sold]), 'Date Table'[Date])

YTD Reviews =
TOTALYTD(SUM(Amazon_Data[Number of Reviews]), 'Date Table'[Date])

% YTD Sales =
DIVIDE([YTD Sales], CALCULATE([YTD Sales], ALL(Amazon_Data)))
```

## 🔮 Future Enhancements
- Add profit & margin metrics
- Build a forecasting model
- Add drill-through product pages
- Automate refresh on Power BI Service
- Customer segmentation analytics

## 👨‍💻 Author
Ishan Pillai  
Power BI Developer • Data Analytics • Business Intelligence
