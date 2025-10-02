# Wholesale Revenue Analysis

## Objective
Analyse wholesale orders by **product line**, **month**, and **warehouse**, adjusting for payment fees to calculate **net revenue**.

## Dataset
- Source: Sales data (June–August 2021)
- Columns: order_number, date, warehouse, client_type, product_line, quantity, unit_price, total, payment, payment_fee
- Filtered: `client_type = 'Wholesale'`

## Method
- SQL query used to calculate `net_revenue = total * (1 - payment_fee)`
- Data exported as `result.csv` and analysed in Python
- Created visualisations in pandas + matplotlib

## Visualizations
1. **Styled stacked bar chart**: Overall wholesale revenue by product line & warehouse
2. **Faceted stacked bar charts**: Separate charts for June, July, August

## Insights
- Central warehouse consistently generates the highest wholesale revenue.
- Engine and Frame & Body parts are the largest revenue drivers.
- Seasonal variation: revenue dips in July for some product lines, then rebounds in August.

## Conclusion
The company should focus on supporting the **Central warehouse** operations and expanding inventory of **high-margin product lines** such as Engine and Frame & Body parts.

## Files
- `Wholesale_Revenue_Analysis.ipynb` — Notebook with full analysis & charts
- `result.csv` — Query result data
