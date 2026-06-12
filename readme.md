# UrbanCart Retail Shop Analytics Project



### Project Overview

UrbanCart is a growing online retail company operating across multiple cities and selling a wide range of consumer products. As the business continues to process a large volume of customer orders, management wants to use data more effectively to improve revenue, understand customer behavior, optimize product performance, manage inventory risk, and evaluate payment preferences.

This project uses SQL-based analysis to examine UrbanCart’s transactional business data and answer 25 real-world business questions. The analysis focuses on sales performance, customer segmentation, product revenue contribution, order status, cancellation behavior, stock-out risk, product bundling opportunities, and payment method usage.

The final goal of this project is to convert raw transactional data into meaningful business insights that can support data-driven decision-making.

### 🧠 Project Goal

To use SQL to analyze UrbanCart’s transactional retail data and convert it into meaningful business insights that help management improve revenue, understand customer behavior, optimize inventory, evaluate product performance, and support better business decisions.

### Project Objectives

The main objectives of this project are:

* Analyze UrbanCart’s total sales, orders, revenue, and customer activity.
* Identify top-performing cities, products, categories, and customers.
* Understand customer purchasing behavior across time, gender, city, and account age.
* Evaluate order status patterns, including completed, pending, and cancelled orders.
* Detect inventory risks by identifying products with high sales volume and low stock.
* Analyze payment method usage and its relationship with order value and order status.
* Identify frequently purchased product pairs for bundling and recommendation strategies.
* Generate daily, monthly, and operational reports for business monitoring.
* Provide actionable business recommendations based on the analysis.

### Business Questions Addressed

This project answers 25 business questions, including:

1. Total number of orders received.
2. Cities generating the highest orders and revenue.
3. Percentage of customers using Gmail.
4. Monthly trend of total orders.
5. Completed, pending, and cancelled order rates.
6. Total revenue generated.
7. Product categories contributing most to revenue.
8. Highest revenue-generating products.
9. Average order value and average basket size.
10. Products at risk of stock-out.
11. Highest revenue-contributing customers.
12. Cancellation rate by city and customer.
13. Purchasing pattern differences by gender and category.
14. Customer behavior over time since account creation.
15. Customers who ordered in October but not December.
16. Customers who ordered in both October and December.
17. Most frequently used payment methods.
18. Relationship between payment method and order status.
19. City-level payment method preferences.
20. Payment methods associated with higher-value orders.
21. Average items per order by payment method.
22. Difference between category average price and product price.
23. Most frequently purchased product pairs.
24. Product pairs generating the highest combined revenue.
25. Daily business report including orders, items, completed orders, cancelled orders, and revenue.

### Repository Structure

```text
UrbanCart-Retail-Analytics/
│
├── README.md
│
├── sql_code_for_analysis
│
├── DataSet/
│   ├── DimCustomers.csv
│   ├── DimProducts.csv
│   ├── FactOrder.csv
│   ├── FactOrderItems.csv
│   └── FactPayment.csv
│
├── Images/
│   ├── monthly_order_trend.png
│   ├── revenue_by_category.png
│   ├── top_products_by_revenue.png
│   ├── payment_method_usage.png
│   └── city_revenue_performance.png
│
└── docs/
    └── er_diagram.png
```

### Analysis Insight With Business Questions
This section evaluates UrbanCart’s overall business performance by analyzing total orders, total revenue, average order value, monthly order trends, city-wise revenue, and daily business activity.

#### 1. Sales Performance Analysis
1. **Total number of orders received.**
   
   | Metric               | Value  |
|---------------------|-------|
| Total Orders Received | 1,200 |

3. **Cities generating the highest orders and revenue**
4. **Monthly trend of total orders**
5. **Completed, pending, and cancelled order rates**
6. **Total revenue generated**
7. **Product categories contributing most to revenue**
8. **Highest revenue-generating products**
9. **Average order value and average basket size**
5. **Daily business report including orders, items, completed orders, cancelled orders, and revenue**

#### 2. Customer Behavior Analysis
This section examines customer contribution, Gmail usage, repeat purchasing behavior, customer activity across months, purchasing behavior since account creation, and differences in purchasing patterns by gender and city.

3. **Percentage of customers using Gmail**
12. **Cancellation rate by city and customer**
14. **Customer behavior over time since account creation**
15. **Customers who ordered in October but not December**
16. **Customers who ordered in both October and December**

#### 3. Product and Category Performance
This section identifies the best-performing product categories and individual products based on revenue and sales volume. It also compares product prices with category average prices to understand pricing differences.

7. **Product categories contributing most to revenue**
8. **Highest revenue-generating products**
13. **Purchasing pattern differences by gender and category**
22. **Difference between category average price and product price**

#### 4. Inventory Risk Analysis
This section identifies products that may be at risk of stock-out by comparing sales volume with available inventory. These insights can help UrbanCart improve inventory planning and avoid lost sales.

10. **Products at risk of stock-out**

#### 5. Payment Method Analysis
This section evaluates which payment methods are used most frequently, whether payment method is related to order status, which cities prefer specific payment methods, and whether higher-value orders are associated with particular payment methods.

17. **Most frequently used payment methods**
18. **Relationship between payment method and order status**
19. **City-level payment method preferences**
20. **Payment methods associated with higher-value orders**
21. **Average items per order by payment method**

#### 6. Product Pair and Basket Analysis
This section identifies products frequently purchased together in the same order and product pairs that generate the highest combined revenue. These findings can support cross-selling, bundling, and recommendation strategies.

23. **Most frequently purchased product pairs**
24. **Product pairs generating the highest combined revenue**


### Key Insights and Findings

The analysis is expected to generate insights such as:

* Which cities are the strongest revenue contributors.
* Which product categories drive the majority of revenue.
* Which products should be prioritized for promotion or inventory planning.
* Which customers contribute the highest lifetime revenue.
* Whether cancellations are concentrated in specific cities or customer groups.
* Which payment methods are most reliable or associated with higher order values.
* Which product pairs can be used for bundle offers and recommendation campaigns.
* Whether customer activity increases or decreases over time after account creation.

### Visualizations

The project includes charts and visualizations to support business storytelling, such as:

* Monthly order trend chart.
* Revenue by city.
* Revenue by product category.
* Top products by revenue.
* Payment method usage distribution.
* Completed, pending, and cancelled order rate.
* Daily order and revenue trend.
* Frequently purchased product pairs.

### Business Recommendations

Based on the analysis, UrbanCart can take the following actions:

* Focus marketing campaigns on cities with high revenue and strong order volume.
* Promote top-performing categories and products through targeted campaigns.
* Monitor high-demand, low-stock products to reduce stock-out risk.
* Use product-pair analysis to create bundle offers and personalized recommendations.
* Investigate cities or customers with high cancellation rates.
* Improve payment experience by prioritizing the most frequently used and successful payment methods.
* Track daily and monthly trends to support operational planning.
* Use high-value customer analysis to design loyalty and retention programs.

### Tools Used

| Tool   | Purpose |
|--------|---------|
| SQL | Data cleaning, scoring, filtering |
| RDBMS | Connect multiple table data |
| Excel  | Visualization & Pivoting |
| Python | Visualization |
| ER Diagram tool | ERD Visualization |
|GitHub | Store, track, collaborate & manage data analysis |


## Final Deliverables

The project deliverables include:

* SQL scripts answering all 25 business questions.
* README documentation explaining the project and findings.
* Output tables or result files.
* Charts and visualizations.
* ER diagram.
* Business recommendations based on analytical findings.

## Important Note

This README does not include SQL code. All SQL queries are stored separately in the `sql_code_for_analysis` file, following the project requirements.

## Conclusion

This project demonstrates how SQL can be used to analyze retail transaction data and generate business insights. The analysis supports UrbanCart’s goals of improving revenue, understanding customer behavior, optimizing inventory, strengthening product strategy, and making better operational decisions.


## Dataset Overview

This repository contains a structured **e-commerce sales dataset** designed for SQL practice, data cleaning, exploratory data analysis, dashboard development, and business-intelligence projects.

The dataset represents customer orders, purchased products, order-level details, and selected payment methods within a Bangladesh-oriented retail context.

It follows a relational data model with dimension and fact tables. The dataset can be used to analyse sales performance, customer behaviour, product demand, order-status trends, payment-method preferences, and operational performance.

---

### Dataset Summary

| Metric              |                                Value |
| ------------------- | -----------------------------------: |
| Total Customers     |                                  100 |
| Total Products      |                                   41 |
| Total Orders        |                                1,200 |
| Total Order Items   |                                4,621 |
| Total Units Ordered |                               11,509 |
| Product Categories  |                                   12 |
| Payment Methods     |                                    5 |
| Order Date Range    | 14 September 2025 – 12 December 2025 |

---

### Dataset Files

| File Name            |  Rows | Description                                                                                                      |
| -------------------- | ----: | ---------------------------------------------------------------------------------------------------------------- |
| `DimCustomers.csv`   |   100 | Contains customer profile information, including name, gender, email, phone number, city, and registration date. |
| `DimProducts.csv`    |    41 | Contains product details, including product name, category, unit price, and stock quantity.                      |
| `FactOrders.csv`     | 1,200 | Contains order-level information, including customer reference, order date, and order status.                    |
| `FactOrderItems.csv` | 4,621 | Contains product-level line items for each order, including ordered quantity.                                    |
| `FactPayment.csv`    | 1,200 | Contains the selected payment method linked to each order.                                                       |

---

### Table Schema

##### `DimCustomers.csv`

| Column        | Description                         |
| ------------- | ----------------------------------- |
| `customer_id` | Unique identifier for each customer |
| `full_name`   | Customer name                       |
| `Gender`      | Customer gender                     |
| `email`       | Customer email address              |
| `phone`       | Customer contact number             |
| `city`        | Customer location                   |
| `created_at`  | Customer registration date          |

##### `DimProducts.csv`

| Column         | Description                                         |
| -------------- | --------------------------------------------------- |
| `product_id`   | Unique identifier for each product                  |
| `product_name` | Product name                                        |
| `category`     | Product category                                    |
| `unit_price`   | Current listed price of the product                 |
| `stock`        | Available stock value recorded in the product table |

##### `FactOrders.csv`

| Column        | Description                                                  |
| ------------- | ------------------------------------------------------------ |
| `order_id`    | Unique identifier for each order                             |
| `customer_id` | Customer associated with the order                           |
| `order_date`  | Date on which the order was placed                           |
| `status`      | Current order status: `Completed`, `Pending`, or `Cancelled` |

##### `FactOrderItems.csv`

| Column          | Description                               |
| --------------- | ----------------------------------------- |
| `order_item_id` | Unique identifier for each order-item row |
| `order_id`      | Order associated with the line item       |
| `product_id`    | Product included in the order             |
| `quantity`      | Number of units ordered                   |

##### `FactPayment.csv`

| Column       | Description                                        |
| ------------ | -------------------------------------------------- |
| `payment_id` | Unique identifier for each payment-method record   |
| `order_id`   | Order associated with the payment-method selection |
| `method`     | Selected payment method                            |

---

### Data Model Relationships

![Entity Relation Diagram](Images/UrbanCartERD.jpg)

---

### Order Status Distribution

| Order Status | Number of Orders | Percentage |
| ------------ | ---------------: | ---------: |
| Completed    |              713 |     59.42% |
| Cancelled    |              246 |     20.50% |
| Pending      |              241 |     20.08% |
| **Total**    |        **1,200** |   **100%** |

---

### Payment Methods

![Orders By Method](Images/orders_by_method.png)


---

### Product Categories

The dataset includes products from 12 categories:

* Grocery
* Beverages
* Personal Care
* Fashion
* Home Care
* Digital
* Snacks
* Health
* Electronics
* Meat
* Poultry
* Dairy
![total products in category](Images/product_category_count.png)

---

---

### Data Quality Notes

The relationships between the tables are structurally consistent:

* Each order is linked to a valid customer.
* Each order item is linked to a valid order and product.
* Every order contains at least one order-item record.
* Every order has one linked payment-method record.
* No duplicate primary keys were identified.

However, several limitations should be considered:

1. The order-item table does not store the historical selling price at the time of purchase. Any sales calculation based on `unit_price` should be described as a **gross sales estimate** or **gross sales proxy**.
2. The payment table stores the selected payment method but does not include payment amount, payment status, transaction timestamp, or refund information.
3. The stock column does not include an inventory movement history.
4. Some customer registration dates are missing.
5. Customer phone numbers should be validated and cleaned before using them for operational purposes.

---

#### Important Note

This dataset should be treated as a learning or portfolio dataset. It should not be used for official financial reporting without adding transaction-level prices, verified payment information, inventory movements, and stronger data-quality controls.
