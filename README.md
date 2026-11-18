# Amazon India Sales Dashboard

An Excel management dashboard built for Manoj to present to his manager, Ravi (non-technical). It brings sales, profit, products, orders, customer order status, payment, fulfilment and geographic performance onto one page, using simple charts and KPIs.

Built for **SapphireIQ** from the Amazon India Dashboard business requirements.

## Files

| File | Description |
|---|---|
| `Amazon_India_Dashboard.xlsx` | Final dashboard (3 sheets: Dashboard, Calculations, Data) |
| `Amazon_Sales_Data_India.xlsx` | Source dataset |
| `Amazon_India_Dashboard_Sapphire_IQ.pdf` | Business requirements |

## Dataset

- 10,000 orders, 1 Jan 2024 to 30 Aug 2026
- 13 columns: Order ID, Order Date, Category, Product, Quantity, Unit Price, Discount %, Total Sales, Profit, Payment Method, Fulfilment, Order Status, Ship State
- 5 categories, 25 products, 10 states; no missing values or duplicate orders

## Dashboard sections

1. **Overall Sales & Profit Performance**: Total Sales, Total Profit, Total Orders, Units Sold, Average Order Value, Profit Margin %, and the monthly sales and profit trend
2. **Category & Product Performance**: category-wise sales, profit and units sold, and the Top 10 products by sales
3. **Order Status & Revenue Loss**: Delivered, Shipped, Returned and Cancelled orders, Return Rate %, Cancellation Rate %, and category-wise returns and cancellations
4. **Payment, Fulfilment & Geographic Performance**: sales and profit by payment method and by fulfilment method, and state-wise sales, profit and orders

Each section ends with an auto-generated plain-English insight.

## Key findings

- Total sales of **₹15.58 Cr** and total profit of **₹3.32 Cr**, a **21.3%** profit margin
- Jan to Aug 2026 sales are **8.1% higher** and profit **10.2% higher** than the same period in 2025
- **Electronics & Mobiles** drives about 79% of sales
- **9.9%** of orders were returned or cancelled, about **₹1.56 Cr (10% of sales)** that earned no profit
- **UPI** accounts for about 50% of sales, and **Amazon FBA** fulfils 69% of sales
- **Maharashtra** is the top state, and the top 3 states bring about 49% of sales

## How it's built

- **Data**: the raw orders plus an Order Month helper column
- **Calculations**: every KPI and chart table, computed with Excel formulas (`SUMIFS`, `COUNTIFS`, `INDEX/MATCH`, `LARGE`)
- **Dashboard**: KPI tiles, charts and insight text linked to the Calculations sheet

All numbers are live formulas, so the dashboard updates if the data changes.

## Assumptions

- **Total Sales** is the gross order value of all orders, including returned and cancelled ones
- Returned and cancelled orders show zero profit in the source data
- Return Rate % = Returned orders ÷ Total orders (same logic for Cancellation Rate %)
- Charts are shown in ₹ Lakh (1,00,000) and KPI tiles in ₹ Crore (1,00,00,000)

## Tools

Microsoft Excel (formulas and charts)
