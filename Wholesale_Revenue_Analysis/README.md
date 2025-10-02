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
- Central warehouse dominates revenue across most product lines
- Engine, Frame & Body generate the largest revenues
- Seasonal variation visible (June higher than July for some lines)

## Files
- `Wholesale_Revenue_Analysis.ipynb` — Notebook with full analysis & charts
- `result.csv` — Query result data
