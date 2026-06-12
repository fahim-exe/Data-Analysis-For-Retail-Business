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

---

8. **Highest revenue-generating products**

**Business Question:**  
Which individual products generate the highest revenue?

**Analysis:**  
Revenue was calculated at the individual product level to identify the products contributing the most to UrbanCart's sales performance.

| Product Name | Category | Total Revenue (BDT) |
|-------------|----------|--------------------:|
| Power Bank 10000mAh | Electronics | 183,350 |
| Nazirshail Rice 5kg | Grocery | 107,120 |
| Horlicks 500g | Health | 87,360 |
| Wallet (Men) | Fashion | 80,100 |
| Ladies Bag | Fashion | 71,400 |

**Visualization:**  
<img width="2968" height="1768" alt="q8_top_products_revenue" src="https://github.com/user-attachments/assets/f526e6c5-e99f-4508-a3c8-32a959789499" />

**Interpretation:**  
The analysis shows that **Power Bank 10000mAh** is UrbanCart's highest revenue-generating product, generating **BDT 183,350**, significantly outperforming all other products. This indicates strong customer demand within the Electronics category.

Among non-electronic products, **Nazirshail Rice 5kg** emerged as the strongest performer, highlighting the importance of Grocery products in overall revenue generation. Fashion products such as **Wallet (Men)** and **Ladies Bag** also contributed substantially, demonstrating strong customer interest in lifestyle and personal-use items.

The presence of products from Electronics, Grocery, Health, and Fashion among the top revenue generators suggests that UrbanCart's revenue is diversified across multiple categories rather than being dependent on a single product segment.

**Business Recommendations:**  
1. Maintain adequate inventory levels for top-performing products to avoid stock-outs.
2. Use high-revenue products as featured products in promotional campaigns.
3. Implement cross-selling strategies for customers purchasing Power Banks and other electronics.
4. Bundle top-performing grocery and health products to increase basket value.
5. Monitor product-level revenue regularly to identify emerging best-sellers and declining products.

---

9. **Average order value and average basket size**
**Business Question:**  
What is the average order value (AOV) and average basket size?

**Analysis:**  
From the transactional data, we calculated:

| Metric | Value |
|--------|-------|
| Average Order Value (BDT) | 1,824.13 |
| Average Basket Size (items) | 9.54 |

**Interpretation:**  
- The **average order value** of BDT 1,824 indicates the typical revenue generated per order.  
- The **average basket size** of approximately 9.5 items shows that customers usually purchase multiple products per transaction.  
- Together, these metrics provide insight into customer purchasing behavior and can help forecast revenue, design promotions, and optimize pricing.

**Business Recommendations:**  
1. Encourage upselling or cross-selling to increase average basket size and order value.  
2. Identify product combinations frequently bought together to create bundle offers.  
3. Monitor trends in AOV and basket size over time to detect shifts in customer behavior or impact of promotions.  
4. Segment customers by AOV and basket size for targeted loyalty programs.
---
25. **Daily business report including orders, items, completed orders, cancelled orders, and revenue**
**Business Question:**  
Generate a daily report containing Date, Total Orders, Total Items, Completed Orders, Cancelled Orders, and Total Revenue.

**Analysis:**  
The daily transactional data was summarized as follows:

| Date       | Total Orders | Total Items | Completed Orders | Cancelled Orders | Total Revenue (BDT) |
|-----------|-------------:|------------:|----------------:|----------------:|------------------:|
| 2025-09-14 | 15          | 102         | 15              | 0               | 16,077            |
| 2025-09-15 | 11          | 78          | 10              | 1               | 9,754             |
| 2025-09-16 | 14          | 91          | 11              | 3               | 17,661            |
| 2025-09-17 | 21          | 143         | 19              | 2               | 22,783            |
| 2025-09-18 | 8           | 52          | 7               | 1               | 4,559             |


**Visualization:** 
<img width="3565" height="1768" alt="qn25_daily_report" src="https://github.com/user-attachments/assets/83a84f99-6073-4ea9-aedb-1f962638af64" />


**Interpretation:**  
- Daily order volume and revenue fluctuate across the period, indicating variability in customer demand.  
- Completed orders dominate daily transactions, but cancelled orders occur intermittently, highlighting the need to monitor cancellations closely.  
- Total revenue generally aligns with total orders and total items sold, indicating consistency in average order value.  
- This daily report allows stakeholders to track operational performance, identify high and low activity days, and respond to trends in real-time.

**Business Recommendations:**  
1. Use the daily report to proactively manage inventory and staffing levels.  
2. Investigate days with higher cancellations to mitigate operational issues.  
3. Analyze daily trends to plan promotions or campaigns on slower days.  
4. Integrate the daily report into dashboards for continuous monitoring of orders and revenue.
 


---


#### 2. Customer Behavior Analysis

This section examines customer contribution, mail usage, repeat purchasing behavior, customer activity across months, purchasing behavior since account creation, and differences in purchasing patterns by gender and city.

---
3. **Percentage of customers using Gmail**
**Business Question:**  
What percentage of total customers use Gmail?

**Analysis:**  
Customer email provider data shows:

| Email Provider | Total Customers | Percentage (%) |
|---------------|----------------|----------------|
| Gmail         | 76             | 76.0           |
| Outlook       | 11             | 11.0           |
| Yahoo         | 13             | 13.0           |

**Visualization:**  
<img width="2374" height="1408" alt="q3_customer_distribution_by_email_provider" src="https://github.com/user-attachments/assets/54e8b89e-5e3f-4b28-a9f8-a9f5d203e3d4" />


**Interpretation:**  
- **Gmail** is the dominant email provider among UrbanCart customers, with **76%** of users.  
- Outlook and Yahoo represent smaller segments, with 11% and 13% respectively.  
- This indicates that marketing campaigns, account-related notifications, and promotions can be primarily optimized for Gmail users.  
- Understanding email provider distribution helps in segmenting customers for email campaigns, personalization, and deliverability optimization.

**Business Recommendations:**  
1. Optimize email campaigns for Gmail to reach the majority of customers.  
2. Test email templates across smaller providers (Outlook/Yahoo) to ensure deliverability and consistency.  
3. Monitor email engagement by provider to refine communication strategy.


---
12. **Cancellation rate by city and customer**
**Business Question:**  
Generate a list of cancellation rate by city.

**Analysis:**  
Cancellation rate was calculated by comparing cancelled orders against total orders for each city.

| City | Total Orders | Cancelled Orders | Cancellation Rate (%) |
|------|-------------:|-----------------:|----------------------:|
| Gazipur | 103 | 28 | 27.18 |
| Rangpur | 121 | 30 | 24.79 |
| Barishal | 173 | 42 | 24.28 |
| Rajshahi | 126 | 29 | 23.02 |
| Dhaka | 81 | 17 | 20.99 |
| Khulna | 121 | 24 | 19.83 |
| Sylhet | 148 | 26 | 17.57 |
| Narayanganj | 61 | 10 | 16.39 |
| Chattogram | 140 | 22 | 15.71 |
| Cumilla | 126 | 18 | 14.29 |

**Visualization:**  
<img width="2959" height="1768" alt="qn12_cancellation_rate_by_city" src="https://github.com/user-attachments/assets/05ffa24a-125a-4123-a32d-5c43695d424b" />


**Interpretation:**  
Gazipur has the highest cancellation rate at **27.18%**, followed by Rangpur and Barishal. This suggests that these cities may have operational, delivery, stock availability, or customer commitment issues. Cumilla and Chattogram show the lowest cancellation rates, indicating relatively stronger order completion performance.

**Business Recommendations:**  
1. Investigate cancellation reasons in Gazipur, Rangpur, and Barishal.
2. Check whether cancellations are linked to payment method, delivery delay, or stock availability.
3. Improve customer communication before delivery confirmation.
4. Monitor city-level cancellation rates regularly as an operational KPI.



---
14. **Customer behavior over time since account creation**
**Business Question:**  
How does customer purchasing behavior change over time since account creation?

**Data Quality Note:**  
Two versions of the analysis were created:

- **Taking every value:** Missing `created_at` values were filled using the customer's earliest order date.
- **Omitting null values:** Customers with missing `created_at` values were excluded from the analysis.

**Analysis: With Null Values Handled**

| Account Age Bucket | Active Customers | Completed Orders | Orders per Active Customer | Avg Units per Order | Avg Order Value Proxy | Gross Sales Proxy |
|---|---:|---:|---:|---:|---:|---:|
| 0-30 days | 96 | 290 | 3.02 | 9.54 | 1,801.86 | 522,539 |
| 31-60 days | 96 | 241 | 2.51 | 9.52 | 1,794.71 | 432,524 |
| 61-90 days | 80 | 182 | 2.28 | 9.57 | 1,898.60 | 345,545 |

**Analysis: Without Null Created Date Rows**

| Account Age Bucket | Active Customers | Completed Orders | Orders per Active Customer | Avg Units per Order | Avg Order Value Proxy | Gross Sales Proxy |
|---|---:|---:|---:|---:|---:|---:|
| 0-30 days | 88 | 272 | 3.09 | 9.53 | 1,791.47 | 487,279 |
| 31-60 days | 88 | 225 | 2.56 | 9.58 | 1,816.63 | 408,742 |
| 61-90 days | 73 | 167 | 2.29 | 9.56 | 1,828.59 | 305,375 |

<img width="2957" height="1768" alt="qn14_customer_behavior_account_age" src="https://github.com/user-attachments/assets/17743be1-3fb5-4128-b775-627759abdbd3" />


**Interpretation:**  
Customer purchasing activity is strongest within the first **0-30 days** after account creation. In both versions of the analysis, orders per active customer decline as account age increases. This suggests that newer customers are more active shortly after registration, but engagement gradually decreases over time.

Average units per order remain stable across all account-age groups, which means customers continue to buy a similar number of items per order. However, total completed orders and gross sales proxy decrease in older account-age groups, mainly due to lower customer activity.

The version with null values handled gives a broader customer view, while the version excluding null values is cleaner but removes some customer records. For business reporting, the **w_null version is more useful**, but the imputation method should be clearly documented.

**Business Recommendations:**  
1. Strengthen customer retention campaigns after the first 30 days.
2. Send personalized offers to customers entering the 31-60 day period.
3. Track repeat purchase rate by account-age bucket.
4. Use the `w_null` version for business interpretation, but keep the `wo_null` version for data-quality validation.
5. Improve customer registration data collection to reduce missing `created_at` values.





---
15. **Customers who ordered in October but not December**


**Business Question:**  
Generate a list of customers who ordered in October but did not place any orders in December.

**Analysis:**  
A customer retention analysis was performed to identify customers who were active during October but became inactive in December.

| Metric | Value |
|---------|------:|
| Customers Ordered in October but Not in December | 17 |

<img width="500" height="210" alt="image" src="https://github.com/user-attachments/assets/ba8b935e-84d6-442e-b883-fce13f0ff87d" />



**Interpretation:**  
A total of **17 customers** placed orders during October but did not return to make any purchases in December. These customers represent a potential churn segment because they demonstrated purchase intent previously but did not continue their engagement with UrbanCart.

The presence of inactive customers over a relatively short period may indicate declining customer engagement, competitive alternatives, reduced purchase frequency, or a lack of effective retention strategies.

Identifying these customers provides an opportunity for targeted remarketing campaigns and personalized promotions to reactivate their purchasing behavior.

**Business Recommendations:**  
1. Launch re-engagement campaigns targeting these inactive customers.
2. Offer personalized discounts or promotional vouchers to encourage repeat purchases.
3. Analyze their previous purchase categories to recommend relevant products.
4. Implement customer lifecycle monitoring to identify churn risk earlier.
5. Track repeat purchase rates as a key customer retention KPI.
---


16. **Customers who ordered in both October and December**


---
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
