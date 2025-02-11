# Sales Data Analysis - Power BI Dashboard

## 📅 Project Overview

The **Sales Data Analysis** project is a Power BI dashboard designed to help businesses monitor their sales performance, identify trends, and make data-driven decisions. This dashboard provides a comprehensive analysis of revenue generation, product sales, customer behavior, and regional performance.

## 💪 Business Objectives

- Identify top-performing and underperforming products and categories.
- Analyze sales trends over different time periods (daily, monthly, quarterly, annually).
- Monitor revenue and profit margins.
- Understand customer purchasing behavior and retention.
- Evaluate the impact of discounts on sales and profitability.
- Provide an interactive, visually appealing dashboard for decision-making.

## 📊 Key Features & Insights

### **1. Product Performance Analysis**

- **Top/Bottom 5 Products:** Identified based on sales, profit, and quantity sold.
- **Most Profitable Products:** Highlighting high-margin products that drive revenue.
- **Underperforming Products:** Products with low sales volume and profit margins, helping businesses optimize inventory.

![Product Performance Analysis](Assets/2.Top&Bottom%205%20Analysis.png)

### **2. Sales Trends Analysis**

- **Monthly & Quarterly Sales Trends:** Clear patterns in revenue fluctuations over time.
- **Seasonal Sales Impact:** Identified peak sales periods and seasonal buying behavior.
- **Day-of-Week Trends:** Determined which days drive the most revenue, optimizing marketing efforts.

![Sales Trends Analysis](Assets/3.Comparison%20Sales&Profit.png)

### **3. Revenue & Profitability Metrics**

- **Total Revenue & Profit Tracking:** Monitoring trends in income and expenses.
- **Profit Margin Analysis:** Identifying areas where cost reductions could improve profitability.
- **Sales & Profit Correlation:** Understanding which products/services generate the most profit relative to revenue.

### **4. Customer Behavior & Retention**

- **Customer Segmentation:** Categorized customers based on purchase frequency and spending behavior.
- **Repeat Customer Analysis:** Determined customer retention rates and their contribution to revenue.
- **High-Value Customers:** Identified customers who generate the highest revenue, helping tailor marketing strategies.

### **5. Discount Impact Analysis**

- **Average Discount by Category:** Evaluated discount effectiveness and how it influences sales volume.
- **Discount vs. Profitability:** Determined whether discounting strategies lead to increased revenue or margin loss.
- **Optimal Discount Rate:** Suggested discount thresholds that maximize both sales and profits.

### **6. Regional Sales Analysis**

- **Top Performing Locations:** Cities/regions with the highest sales contributions.
- **Low-Performing Areas:** Identified underperforming locations and potential reasons (demographics, competition, etc.).
- **Geo-Heat Map Visualization:** Used Power BI maps to visually display revenue distribution.

![Regional Sales Analysis](Assets/1.Overview.png)

## 📚 Dataset Overview

### **Tables Used**

- **Sales Data:** Contains transaction details including date, product ID, customer ID, quantity, price, and revenue.
- **Customers:** Stores customer information such as name, location, and purchase frequency.
- **Products:** Includes product details like name, category, cost, and profit margin.
- **Regions:** Provides geographical sales distribution.

### **Key Metrics & Measures (DAX)**

```DAX
Quantity Sold = CALCULATE(SUM('Fact Table'[Units Sold]), ALL('Date Table 1'), USERELATIONSHIP('Date Table 2'[Date], 'Fact Table'[Date (dd/mm/yyyy)]))

Sum Dim = SUM('Fact Table'[Net Sales])

Sum of Net Sales = CALCULATE(SUM('Fact Table'[Net Sales]), ALL('Date Table 1'), USERELATIONSHIP('Date Table 2'[Date], 'Fact Table'[Date (dd/mm/yyyy)]))

Total Profit = CALCULATE(SUM('Fact Table'[Profit]), ALL('Date Table 1'), USERELATIONSHIP('Date Table 2'[Date], 'Fact Table'[Date (dd/mm/yyyy)]))
```

## 🛠️ Technologies Used

- **Power BI** for data visualization and interactive dashboards.
- **DAX (Data Analysis Expressions)** for custom calculations and data modeling.
- **Excel/CSV** as the data source.

## 🚀 How to Use

1. Download the `Sales Data Analysis.pbix` file.
2. Open it in **Power BI Desktop**.
3. Explore the dashboard using filters and slicers.
4. Analyze key metrics, trends, and insights to drive business decisions.

## 🎨 Dashboard Screenshots

![Table Visual](Assets/4.Table%20Visual.png)

## 🏆 Future Improvements

- Implement **real-time data updates** to keep sales metrics up to date.
- Enhance **predictive analytics** using machine learning for sales forecasting.
- Optimize **DAX calculations** for better performance and faster report loading.
- Develop **automated alerts** for unusual sales trends or stock shortages.


