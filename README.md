# E-commerce Sales Analysis

A data analysis project in Python that looks at 500 e-commerce orders placed across India in 2025, and answers: what sells, where, when, and how much profit it really brings.

## Project files
- `ecommerce_sales_analysis.ipynb`: the full analysis notebook (code, charts and written insights)
- `python_ecommerce_sales_dataset.csv`: the dataset

## Dataset
500 orders, 16 columns:

| Column | Description |
|---|---|
| Order_ID, Order_Date, Customer_ID | Order and customer identifiers, order date |
| Customer_Segment | Consumer, Corporate or Small Business |
| Region, City | Where the order was placed |
| Sales_Channel | Website, Marketplace or Mobile App |
| Product, Category | What was sold |
| Quantity, Unit_Price_INR, Discount_Percent | Order details |
| Sales_INR, Profit_INR | Revenue and profit of the order |
| Payment_Method, Order_Status | Payment type, and Delivered / Cancelled / Returned |

## What I did
1. **Explored** the data (shape, types, summary statistics)
2. **Cleaned** it (duplicates, missing values, date conversion, trimming text columns)
3. **Analysed** order status, region, category, monthly trend, top products, discounts, sales channel and customer segment
4. **Visualised** the results with matplotlib
5. **Wrote insights** under every section

Revenue analysis uses **Delivered orders only**, because cancelled orders have no revenue and returned orders lose money.

## Key findings
- Only **59%** of orders were delivered. 20.6% were cancelled and 20.4% were returned. Returned orders caused a loss of about ₹22.5K.
- Delivered orders gave **₹6.42 lakh sales and ₹1.03 lakh profit** (16.05% margin).
- **Electronics** leads in sales (₹2.40 lakh), but **Home & Living** (20.0%) and **Stationery** (26.9%) earn much higher margins. **Fitness** sells well but has a thin 11.6% margin.
- **West** leads in sales, while **East** has the best margin (19.1%).
- Sales peak in **December and March** and drop sharply in **August**.
- **Running Shoes and Bluetooth Speaker** make up 37% of sales. Running Shoes has the lowest margin (7.3%) among the top 10.
- **Discounts hurt profit**: margin falls from 24.9% with no discount to 2.4% at a 20% discount. All 6 loss-making delivered orders are Running Shoes sold at 20% discount.

## Recommendations
- Reduce cancellations and returns, which affect about 4 in 10 orders.
- Limit discounts to around 10%, especially on Running Shoes.
- Push high-margin categories (Home & Living, Stationery) and study what works in the East region.
- Plan stock and campaigns around the August slump and the December peak.

## Tools
Python, pandas, numpy, matplotlib, seaborn, Google Colab

## How to run
1. Open `ecommerce_sales_analysis.ipynb` in Google Colab or Jupyter.
2. Keep `python_ecommerce_sales_dataset.csv` in the same folder as the notebook (in Colab, upload it to the Files panel).
3. Run all cells.
