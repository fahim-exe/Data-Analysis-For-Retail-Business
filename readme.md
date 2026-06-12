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
3. Percentage of customers using email provide.
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

### Analysis Insight With Business Questions
This section evaluates UrbanCart’s overall business performance by analyzing total orders, total revenue, average order value, monthly order trends, city-wise revenue, and daily business activity.

#### 1. Sales Performance Analysis
1. **Total number of orders received.**
   | Metric | Value|
   |---------|-------|
   |Total Number of Orders | 1200 |
   
---

3. **Cities generating the highest orders and revenue**
  The city-level sales analysis shows that Chattogram generated the highest number of orders and the highest total revenue. Barishal and Sylhet also performed strongly, with the same number of orders but slightly different revenue values.

    | City        | Total Orders | Total Revenue |
    |------------|-------------:|--------------:|
    | Chattogram | 99 | 181,812 |
    | Barishal   | 93 | 176,536 |
    | Sylhet     | 93 | 174,507 |
    | Cumilla    | 88 | 172,860 |
    | Rangpur    | 71 | 124,761 |
**Visualization:**  
    <img width="2665" height="1768" alt="q2_completed_orders_by_city" src="https://github.com/user-attachments/assets/c6a2a4f5-78a4-4a18-8e86-9709b4e19064" />
    
    <img width="2662" height="1768" alt="q2_completed_order_gross_sales_proxy_by_city" src="https://github.com/user-attachments/assets/a2016260-101b-4d12-b8c0-e471ef14b4f5" />


**Interpretation:**  
Chattogram is UrbanCart’s strongest city market because it leads in both order volume and revenue. Barishal and Sylhet show strong customer activity, but Barishal generated slightly higher revenue than Sylhet, which may indicate a higher average order value. Rangpur generated the lowest orders and revenue among these cities, suggesting lower market penetration or weaker customer engagement.

**Business Recommendation:**  
UrbanCart should prioritize Chattogram for inventory planning, marketing campaigns, and customer retention programs. Barishal and Sylhet should be targeted with upselling and product recommendation strategies. Rangpur may require promotional campaigns or customer acquisition efforts to increase order volume.

---

4. **Monthly trend of total orders**
   
   **Business Question:**  
What is the monthly trend of total orders over time?

**Analysis:**  
Aggregating orders by month shows the following trend:

| Month     | Total Orders |
|----------|--------------|
| Sep 2025 | 243          |
| Oct 2025 | 413          |
| Nov 2025 | 371          |
| Dec 2025 | 173          |

**Visualization:**  

<img width="2355" height="1408" alt="q4_monthly_order_trend" src="https://github.com/user-attachments/assets/3860a8d1-1078-44e4-8fc5-d2973155f0e0" />

**Interpretation:**  
The highest order volume occurred in **October 2025** (413 orders), indicating peak shopping activity. Orders decreased slightly in **November** and dropped significantly in **December**, which could be due to seasonality, promotions, or other operational factors. September showed a moderate start as the initial month in the dataset.

**Business Recommendations:**  
1. Prepare inventory and logistics for peak months like October.  
2. Investigate reasons for December drop to adjust marketing campaigns or promotions.  
3. Monitor monthly trends to plan staffing, inventory, and marketing efforts more efficiently.

---

5. **Completed, pending, and cancelled order rates**
**Business Question:**  
What is the Completed, Pending & Cancelled Rate?

**Analysis:**  
The order status analysis was conducted to understand the operational performance of UrbanCart and identify the proportion of successfully completed, pending, and cancelled orders.

| Order Status | Total Orders | Rate (%) |
|-------------|-------------:|---------:|
| Completed   | 713          | 59.42%   |
| Cancelled   | 246          | 20.50%   |
| Pending     | 241          | 20.08%   |
| **Total**   | **1,200**    | **100%** |


**Visualization:**  

<img width="2375" height="1408" alt="q5_order_status_distribution" src="https://github.com/user-attachments/assets/62a5e578-ff9c-4383-b989-865c3ed10ba1" />


**Interpretation:**  
- Approximately **59.42%** of all orders were successfully completed, indicating that the majority of customer purchases were fulfilled.
- However, nearly **40%** of orders remain either cancelled or pending, representing a significant operational concern.
- The cancellation rate (**20.50%**) is slightly higher than the pending rate (**20.08%**), suggesting potential issues related to inventory availability, payment completion, customer behavior, or fulfillment processes.
- A high percentage of pending orders may indicate delays in order processing, payment verification, or logistics operations.

**Business Recommendations:**  
1. Investigate the primary reasons behind order cancellations and implement corrective measures.
2. Monitor pending orders closely and establish service-level targets for order processing.
3. Improve customer communication during the order fulfillment process to reduce cancellation risk.
4. Analyze cancellation and pending rates by city, payment method, and product category to identify specific operational bottlenecks.
5. Develop a real-time order status dashboard for proactive monitoring and decision-making.

---

6. **Total revenue generated**
**Business Question:**  
What is the total revenue generated by UrbanCart?

**Analysis:**  
The total revenue was calculated by aggregating revenue across all completed and recorded transactions within the analysis period.

| Metric | Value (BDT) |
|---------|------------:|
| Total Revenue Generated | 1,300,608 |

**Interpretation:**  
UrbanCart generated a total estimated revenue of **BDT 1,300,608** during the analysis period. This figure represents the overall sales performance of the business and serves as a key indicator of commercial success. The revenue generated reflects customer demand across multiple product categories, cities, and payment methods.

As a high-level business KPI, total revenue provides a foundation for evaluating profitability, growth trends, customer value, and operational performance. Further analysis of revenue by city, category, product, customer segment, and payment method can help identify the key drivers contributing to this revenue.

**Business Recommendations:**  
1. Monitor total revenue regularly through executive dashboards.
2. Identify the highest revenue-generating cities and product categories to prioritize investment.
3. Analyze customer segments contributing most to revenue for retention and loyalty initiatives.
4. Track monthly revenue trends to support forecasting and business planning.
5. Combine revenue analysis with profitability metrics to improve strategic decision-making.

--- 


7. **Product categories contributing most to revenue**
**Business Question:**  
Which product categories contribute the most to total revenue?

**Analysis:**  
Revenue was aggregated at the product category level to identify the categories generating the highest sales value.

| Category | Total Revenue (BDT) |
|----------|-------------------:|
| Fashion | 291,670 |
| Grocery | 288,494 |
| Electronics | 219,600 |
| Beverages | 122,575 |
| Personal Care | 94,726 |
| Health | 89,496 |
| Digital | 61,297 |
| Meat | 35,420 |
| Poultry | 30,720 |
| Snacks | 28,160 |
| Home Care | 25,130 |
| Dairy | 13,320 |

**Visualization:**  

<img width="2664" height="1768" alt="q7_category_revenue" src="https://github.com/user-attachments/assets/457de70b-b476-4df3-ad68-c42c9892d840" />


**Interpretation:**  
The analysis reveals that **Fashion** is the highest revenue-generating category, contributing **BDT 291,670**, closely followed by **Grocery** with **BDT 288,494**. Together, these two categories account for a substantial share of UrbanCart's overall revenue. **Electronics** ranks third and represents another major revenue driver.

On the other hand, categories such as **Dairy**, **Home Care**, and **Snacks** contribute relatively little revenue compared to the leading categories. This may indicate lower customer demand, limited product assortment, lower product prices, or fewer transactions within these categories.

The revenue concentration among a few categories suggests that UrbanCart's sales performance is heavily influenced by customer demand in Fashion, Grocery, and Electronics.

**Business Recommendations:**  
1. Prioritize inventory availability for Fashion, Grocery, and Electronics to avoid stock-outs.
2. Increase marketing investment in the top-performing categories to maximize revenue growth.
3. Use cross-selling and bundling strategies between Grocery and complementary categories.
4. Evaluate low-performing categories to determine whether pricing, assortment, or promotional strategies need adjustment.
5. Monitor category-level revenue trends regularly to identify changes in customer preferences.



8. **Highest revenue-generating products**


9. **Average order value and average basket size**


25. **Daily business report including orders, items, completed orders, cancelled orders, and revenue**

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
