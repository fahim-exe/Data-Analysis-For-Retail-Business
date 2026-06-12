# UrbanCart Retail Shop Analytics Project

---

## 📌 Project Overview

UrbanCart is a growing online retail company operating across multiple cities with a diverse product catalog. Management requires data-driven insights to improve revenue, optimize inventory, understand customer behavior, and enhance operational efficiency.

This project uses SQL-based analysis of transactional data to answer **25 real-world business questions**, covering sales performance, customer segmentation, product analytics, payment behavior, inventory risk, and product bundling opportunities.

---

## 🎯 Project Goal

To use SQL and data analytics to convert UrbanCart’s transactional data into meaningful business insights that improve revenue, customer understanding, inventory management, product strategy, and operational decision-making.

---

## 📊 Project Objectives

- Analyze sales, revenue, and order performance
- Identify top-performing cities, customers, and products
- Understand customer behavior across time, gender, and geography
- Evaluate order status and cancellation patterns
- Detect inventory risks and stock-out products
- Analyze payment method usage and behavior
- Identify product bundling opportunities
- Generate operational and daily business reports

---

## 🗂️ Repository Structure

```text
UrbanCart-Retail-Analytics/
│
├── README.md
├── sql_code_for_analysis/
├── DataSet/
├── Images/
└── docs/
```

---

## 📦 Dataset Overview

| Metric | Value |
|--------|------:|
| Total Customers | 100 |
| Total Products | 41 |
| Total Orders | 1,200 |
| Total Order Items | 4,621 |
| Total Units Ordered | 11,509 |
| Categories | 12 |
| Payment Methods | 5 |
| Order Date Range | 14 Sep 2025 – 12 Dec 2025 |

---

## 📊 Key Business Insights

### 1. Sales Performance

#### Total Orders

| Metric | Value |
|--------|------:|
| Total Orders | 1200 |

---

### Top Cities by Revenue

| City | Orders | Revenue |
|------|------:|--------:|
| Chattogram | 99 | 181,812 |
| Barishal | 93 | 176,536 |
| Sylhet | 93 | 174,507 |
| Cumilla | 88 | 172,860 |
| Rangpur | 71 | 124,761 |

📊 Visualization  
<img src="https://github.com/user-attachments/assets/c6a2a4f5-78a4-4a18-8e86-9709b4e19064" />
<img src="https://github.com/user-attachments/assets/a2016260-101b-4d12-b8c0-e471ef14b4f5" />

**Interpretation:** Chattogram leads in orders and revenue. Barishal and Sylhet perform well. Rangpur lags behind.

**Recommendation:** Focus marketing and inventory in Chattogram, upselling in Barishal/Sylhet, promotional campaigns in Rangpur.

---

### Monthly Order Trend

| Month | Orders |
|------|------:|
| Sep | 243 |
| Oct | 413 |
| Nov | 371 |
| Dec | 173 |

📊 Visualization  
<img src="https://github.com/user-attachments/assets/3860a8d1-1078-44e4-8fc5-d2973155f0e0" />

**Interpretation:** October is peak month. December shows drop.

**Recommendation:** Prepare inventory and marketing for October, investigate December drop.

---

### Order Status Distribution

| Status | Rate |
|--------|-----:|
| Completed | 59.42% |
| Cancelled | 20.50% |
| Pending | 20.08% |

📊 Visualization  
<img src="https://github.com/user-attachments/assets/62a5e578-ff9c-4383-b989-865c3ed10ba1" />

**Interpretation:** 59% orders completed; ~40% pending/cancelled.

**Recommendation:** Investigate cancellations, monitor pending orders, improve communication.

---

### Total Revenue

| Metric | Value |
|--------|------:|
| Total Revenue | 1,300,608 BDT |

---

### Revenue by Category

| Category | Revenue |
|----------|--------:|
| Fashion | 291,670 |
| Grocery | 288,494 |
| Electronics | 219,600 |

📊 Visualization  
<img src="https://github.com/user-attachments/assets/457de70b-b476-4df3-ad68-c42c9892d840" />

---

### Top Products

| Product | Revenue |
|----------|--------:|
| Power Bank 10000mAh | 183,350 |
| Nazirshail Rice 5kg | 107,120 |
| Horlicks 500g | 87,360 |

📊 Visualization  
<img src="https://github.com/user-attachments/assets/f526e6c5-e99f-4508-a3c8-32a959789499" />

---

## 👤 Customer Behavior

#### Email Distribution

| Provider | % |
|----------|--:|
| Gmail | 76 |
| Yahoo | 13 |
| Outlook | 11 |

📊 Visualization  
<img src="https://github.com/user-attachments/assets/54e8b89e-5e3f-4b28-a9f8-a9f5d203e3d4" />

#### Customer Retention Risk

- October only: 17  
- October + December: 20+

📊 Visualization  
<img src="https://github.com/user-attachments/assets/ba8b935e-84d6-442e-b883-fce13f0ff87d" />

---

## 💳 Payment Method Insights

### Most Frequently Used

| Payment Method | Orders | Usage (%) |
|----------------|------:|----------:|
| COD | 488 | 40.67 |
| bKash | 349 | 29.08 |
| Nagad | 235 | 19.58 |
| Credit Card | 65 | 5.42 |
| Debit Card | 63 | 5.25 |

📊 Visualization  
<img src="https://github.com/user-attachments/assets/d4556582-e8b9-4ab7-90c2-204314f34c16" />

### Payment Method vs Order Status

📊 Visualization  
<img src="https://github.com/user-attachments/assets/da911385-cf0c-4f6e-974c-cc4ffd9cef2c" />

### City-Level Payment Preferences

📊 Visualization  
<img src="https://github.com/user-attachments/assets/3f9107d0-3c3a-4ce2-981f-1fa92c0f5d14" />

### High-Value Orders by Payment Method

📊 Visualization  
<img src="https://github.com/user-attachments/assets/ecaaf676-6e02-49a0-98ea-fba81d9e1831" />

### Average Basket Size by Payment Method

📊 Visualization  
<img src="https://github.com/user-attachments/assets/fde8bdff-6bd8-4092-8aa3-314bfdabbd86" />

---

## 🧩 Product Pair Analysis

### Most Frequently Purchased Pairs

📊 Visualization  
<img src="https://github.com/user-attachments/assets/c0fc9943-a14e-4194-86a3-768859edbed0" />

### Highest Revenue Product Pairs

📊 Visualization  
<img src="https://github.com/user-attachments/assets/c62b5b0a-ef54-457b-96dc-8154e1d390b3" />

---

## 📌 Key Business Takeaways

- Revenue concentrated in Fashion, Grocery, Electronics  
- COD dominates payment behavior  
- October is peak month  
- Repeat customers engaged  
- Inventory risks for high-demand products  
- Clear bundling opportunities exist  

## 🚀 Recommendations

- Strengthen inventory for top products  
- Improve retention after 30 days  
- Promote digital payments (bKash/Nagad)  
- Focus marketing on top cities  
- Build product bundle strategy  
- Reduce stock-out risk via forecasting  

---

## 🛠 Tools Used

- SQL, Excel, Python (Matplotlib), GitHub, ER Diagram tools

---

## 📌 Conclusion

SQL-based retail analytics enables UrbanCart to make informed decisions on revenue growth, customer retention, and operational efficiency.
