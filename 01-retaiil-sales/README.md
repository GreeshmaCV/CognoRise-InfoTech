# Project 1: Retail Sales Analysis

Data Analytics Internship, CognoRise InfoTech (November 2026 batch)

## Objective

Analyse retail transaction data to understand sales performance, find which products, customer groups and months drive revenue, and turn the findings into business recommendations.

## Dashboard

![Retail Sales Dashboard](dashboard.png)

Demo video: [add your LinkedIn or video link here]

## Dataset

- **Source:** Retail Sales Dataset (Kaggle)
- **Size:** 1,000 transactions, from 1 January 2023 to 1 January 2024
- **Columns:** Transaction ID, Date, Customer ID, Gender, Age, Product Category, Quantity, Price per Unit, Total Amount

## Tools Used

- Microsoft Power BI Desktop (data cleaning in Power Query, DAX measures, dashboard)
- Microsoft Excel (data inspection)

## Data Cleaning

| Check | Result |
|---|---|
| Missing values | None found |
| Duplicate rows | None found |
| Unique IDs | Every Transaction ID and Customer ID is unique |
| Total Amount check | Total Amount equals Quantity x Price per Unit on every row |
| Date column | Converted from text to Date type |

New columns created in Power Query:
- **Month:** month name from the Date column
- **Month Number:** 1 to 12, used to sort months in calendar order
- **Age Group:** 18-25, 26-35, 36-45, 46-55, 56+

Note: one transaction is dated 1 January 2024 and is grouped under January in the monthly view.

## KPIs (DAX Measures)

| KPI | Value |
|---|---|
| Total Revenue | 456,000 |
| Total Quantity | 2,514 units |
| Transactions | 1,000 |
| Average Order Value | 456.00 |

## Dashboard Contents

- 4 KPI cards
- Monthly revenue trend (line chart)
- Revenue by product category (bar chart)
- Revenue by age group (column chart)
- Slicers for Gender and Product Category

## Key Insights

1. **Revenue is balanced across categories.** Electronics (156,905, 34.4%), Clothing (155,580, 34.1%) and Beauty (143,515, 31.5%) are close, so no single category dominates.
2. **Sales are seasonal.** May is the strongest month (53,150), followed by October (46,580) and December (44,690). September is the weakest (23,620), about 55% below May.
3. **High-priced items drive revenue.** Items priced at 300 and 500 are about 40% of transactions but about 88% of revenue (402,900 of 456,000).
4. **Age groups spend differently.** Customers aged 46-55 (100,690) and 26-35 (98,480) bring in the most revenue. The 18-25 group has the highest average order value (500), and it falls with age to 412 for the 56+ group.
5. **Gender split is almost even.** Female customers account for 51.1% of revenue and male customers 48.9%. Women spend more on Clothing, while men spend more on Electronics.

## Business Recommendations

1. **Promote high-priced products** (300 and 500 price points) with featured placement and bundles, since they generate most of the revenue.
2. **Run a campaign in September,** the weakest month, such as discounts or a seasonal offer.
3. **Repeat what works in May, October and February** with similar promotions in slower months.
4. **Target 18-35 customers with premium offers,** since they have the highest order values, and **use bundles or loyalty rewards for the 56+ group** to raise their order value.
5. **Keep stock balanced across all three categories,** as demand is spread evenly.

## Limitations

- The dataset has no cost or profit column, so the analysis covers **revenue only**, not profit.
- There is no region or location column, so Gender and Age Group were used for customer segmentation.
- There is no individual product column, only three categories, so Price per Unit was used as a proxy for product tier.
- The data covers a single year, so seasonal patterns cannot be confirmed over time.

## Files

| File | Description |
|---|---|
| `retail_sales_dataset.csv` | Original dataset |
| `retail_sales_dashboard.pbix` | Power BI dashboard file |
| `retail_sales_dashboard.pdf` | Exported dashboard |
| `dashboard.png` | Dashboard screenshot |
