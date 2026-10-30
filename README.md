# Retail Sales Analysis — 2025

## 1. Project Overview

This project explores a supermarket sales dataset covering January to December 2025.

The aim is to understand sales performance, identify the products and regions generating the most revenue and profit, compare profit margins, and examine sales trends throughout the year.

I used Google Sheets to clean the data, perform calculations, create pivot tables and charts, and build a dashboard to present my findings.

This is an independent practice project created to improve my data analytics skills and build my portfolio.

## 2. Business Problem

The supermarket needs to understand how its products, categories, regions, and sales channels perform.

By analysing the sales data, I aim to identify what contributes most to revenue and gross profit, how sales change over time, and which areas may need further investigation.

The analysis provides insights from the available data. It does not assume that the patterns observed explain why the results occurred.

## 3. Business Questions

The project focuses on the following questions:

1. How much recorded revenue and gross profit did the supermarket generate in 2025?
2. Which products and categories performed best in revenue, sales volume, and gross profit margin?
3. Which regions generated the highest revenue and gross profit?
4. Which sales channels contributed the most revenue and transaction volume?
5. How did revenue change throughout the year?

## 4. Tools Used

* **Google Sheets:** Data cleaning, formulas, calculations, pivot tables, charts, and dashboard creation.
* **GitHub:** Project documentation and portfolio presentation.

## 5. Dataset Overview

The original dataset contained 10,000 transaction records and 12 columns.

The columns included:

* Order ID
* Order Date
* Product
* Category
* Quantity
* Unit Price
* Unit Cost
* Region
* Payment Method
* Sales Channel
* Customer Segment
* Discount Rate

The dataset covers the full 2025 calendar year.

After removing exact duplicate rows, the working dataset contained **9,975 records**.

The dataset is synthetic and was created for practice. It does not represent verified sales records from a real supermarket.

## 6. Data Cleaning and Preparation

Before analysing the data, I checked it for errors and missing information.

### Issues identified

* Duplicate records and repeated order IDs.
* Missing values in Unit Price, Unit Cost, Region, Payment Method, and Customer Segment.
* Inconsistent capitalization in Region and Payment Method.
* Data quality issues that could affect calculations and analysis.

### Cleaning steps completed

1. Checked the dataset's row count, columns, and date range.
2. Identified and removed exact duplicate rows while preserving a backup.
3. Checked that Order IDs were unique after duplicate removal.
4. Standardized capitalization in Region and Payment Method using separate cleaned columns.
5. Checked Quantity, Unit Price, Unit Cost, and Discount Rate for data consistency.
6. Checked for zero or negative values in the numerical fields.
7. Preserved missing values rather than filling them with guesses.

The initial data quality checks identified **121 missing cells** across Unit Price, Unit Cost, Region, Payment Method, and Customer Segment.

Missing financial values were left blank because there was not enough information to determine their correct values.

## 7. Analysis and Calculations

I added calculated fields to understand the supermarket's revenue, costs, and profitability.

### Revenue Before Discounts

Revenue was calculated by multiplying the quantity sold by the unit price.

**Formula:**

Revenue = Quantity × Unit Price

### Net Revenue After Discounts

Net revenue was calculated by applying the recorded discount rate to the revenue before discounts.

**Formula:**

Net Revenue = Quantity × Unit Price × (1 − Discount Rate)

This calculation assumes that Unit Price represents the price before the discount is applied.

### Total Cost

Total cost represents the cost of the units sold.

**Formula:**

Total Cost = Quantity × Unit Cost

### Gross Profit

Gross profit was calculated by subtracting total cost from net revenue.

**Formula:**

Gross Profit = Net Revenue − Total Cost

### Gross Profit Margin

Gross profit margin shows the percentage of net revenue remaining after the recorded product cost is deducted.

**Formula:**

Gross Profit Margin = (Gross Profit ÷ Net Revenue) × 100

For product and category comparisons, I calculated gross profit margin by dividing total gross profit by the corresponding total net revenue for eligible transactions. This avoids incorrectly adding individual transaction margin percentages together.

## 8. Key Findings

### 8.1 Overall Performance

The main financial results were:

| Metric                               |          Result |
| ------------------------------------ | --------------: |
| Records after duplicate removal      |           9,975 |
| Recorded revenue before discounts    | ₦180,057,450.00 |
| Recorded net revenue after discounts | ₦174,907,457.50 |
| Recorded gross profit                |  ₦41,140,207.50 |

These totals do not all cover exactly the same transactions because some records have missing financial values. Gross profit includes transactions for which the required revenue and cost information was available.

### 8.2 Product Performance

The analysis revealed the following:

* **Cooking Gas Refill** generated the highest recorded revenue, at ₦31,762,200.
* **Frozen Chicken** generated the highest recorded gross profit, at ₦5,916,685.
* **Yoghurt** had the highest quantity sold, with 3,002 units.
* **Bottled Water** had the highest recorded gross profit margin, at approximately 58.77%.
* **Cooking Gas Refill** had the lowest recorded gross profit margin among the products, at approximately 16.02%.

These findings show that the product generating the most revenue does not necessarily generate the highest gross profit or the highest profit margin.

### 8.3 Category Performance

The category analysis showed that:

* **Groceries** generated the highest recorded revenue, at approximately ₦64.38 million.
* Groceries also generated the highest recorded gross profit, at ₦14,599,875.
* **Beverages** had the highest recorded gross profit margin among the categories, at approximately 54.9%.
* **Household** had the lowest recorded category gross profit margin, at approximately 18.4%.

This comparison shows the difference between generating a large amount of gross profit and earning a high gross profit margin.

### 8.4 Regional Performance

The regional analysis showed that:

* **Lagos** generated the highest recorded revenue, at ₦50,840,650.
* Lagos also generated the highest recorded gross profit, at ₦11,729,462.50.
* Lagos had the highest recorded gross profit margin among the named regions, at approximately 23.8%.

Some transactions had missing region information. Their results were kept separate rather than assigned to a region without evidence.

The figures show differences in regional performance but do not establish the reasons behind those differences.

### 8.5 Monthly Revenue

Monthly revenue varied throughout 2025.

* **August** recorded the highest revenue, at ₦16,934,350.
* **September** recorded the lowest revenue, at ₦13,562,650.
* The difference between the two months was ₦3,371,700.

This shows that sales performance was not the same throughout the year. Further investigation would be needed to understand what contributed to the difference between the two months.

### 8.6 Sales Channel and Customer Segment Observations

The analysis also revealed that:

* **In-store sales** generated the highest total revenue among the three sales channels, at ₦123,668,700.
* Returning customers contributed the highest total revenue among customer segments with recorded segment information.
* New customers had the highest average transaction value among those segments.

These results describe the available transactions. Additional customer and operational data would be needed to explain why the differences occurred or measure customer retention properly.

## 9. Dashboard

I created a Google Sheets dashboard to bring the main results together in one place.

The dashboard contains three key performance indicators (KPIs):

| KPI                         |          Result |
| --------------------------- | --------------: |
| Total Recorded Revenue      | ₦180,057,450.00 |
| Net Revenue After Discounts | ₦174,907,457.50 |
| Recorded Gross Profit       |  ₦41,140,207.50 |

**The five charts are:**

1. **Monthly Sales Revenue — 2025:** Compares revenue across the 12 months.
2. **Gross Profit Margin by Product:** Compares the profitability of individual products.
3. **Gross Profit Margin by Category:** Compares profitability across product categories.
4. **Revenue by Product:** Shows which products generated the most revenue.
5. **Gross Profit Margin by Region:** Compares gross profit margins across regions.

Together, the dashboard provides an overview of sales trends, product performance, category profitability, and regional margins. The dashboard is designed to help viewers compare performance and identify important patterns quickly.

### Project Workbook

[Download the Retail Sales Analysis Workbook](./retail-sales-analysis-2025.xlsx)

## 10. Practical Recommendations

The following recommendations are based on the observed patterns. They are suggestions for further business consideration, not proven solutions to the causes of the results.

1. **Review product pricing and costs.** Investigate products with lower gross profit margins, particularly Cooking Gas Refill, to understand their cost structures and pricing.

2. **Protect strong-performing categories.** Monitor Groceries, which generated the highest recorded revenue and gross profit, while assessing opportunities to improve other categories.

3. **Investigate regional differences.** Examine product mix, transaction volume, and operating conditions across regions to understand why sales and profitability vary.

4. **Explore opportunities in alternative sales channels.** In-store generates the most total revenue, while Phone Order has the highest average recorded transaction value. Further investigation could help identify opportunities to grow sales through online and phone orders.

5. **Investigate monthly trends.** Review promotions, inventory availability, and customer activity to understand the differences between high- and low-revenue months.

These are suggested actions based on the observed results, not proven explanations for the differences.

## 11. Limitations

There are several limitations to this analysis:

* The dataset is synthetic and does not represent verified sales from a real supermarket.
* Missing Unit Price and Unit Cost values affect the completeness of the revenue and gross profit calculations.
* Missing Region, Payment Method, and Customer Segment values limit some group comparisons.
* Gross profit represents net revenue after discounts less recorded product costs. It is not net profit because other business expenses were not provided.
* The analysis identifies patterns but does not establish why sales or profitability differ across products, regions, sales channels, or months.
* The net revenue calculation assumes that Unit Price is the price before the recorded discount is applied. This assumption should be verified against the dataset documentation where possible.

The results should therefore be interpreted in the context of the available data and its limitations.

## 12. Conclusion

This project gave me practical experience in cleaning a dataset, working with spreadsheet formulas, calculating revenue and gross profit, creating pivot tables, comparing business performance, and building a dashboard.

The analysis revealed differences in product revenue, gross profit margins, category performance, regional results, and monthly sales.

The dashboard presents these findings visually, while the practical recommendations identify areas the supermarket could investigate further.

As a developing data analyst, this project has helped me practise turning raw data into meaningful findings and presenting those findings in a clear and professional way.

This project forms part of my data analytics portfolio and demonstrates my growing skills in Google Sheets, data analysis, and data visualization.

