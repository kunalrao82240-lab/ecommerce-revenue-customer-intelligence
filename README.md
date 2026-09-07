# 🛒 E-Commerce Revenue & Customer Intelligence

An end-to-end data analytics project using the **Olist Brazilian E-Commerce Public Dataset** to analyze revenue, customer behavior, product performance, delivery operations, and business opportunities.

The project follows a complete analytics workflow:

**Raw Data → Python EDA → SQL Analysis → Power BI Dashboard → Business Recommendations**

---

## 📌 Project Overview

E-commerce businesses generate large volumes of transactional data, but raw sales data alone does not explain:

* Which customers generate the most value?
* How effectively does the business retain customers?
* Which product categories drive revenue?
* Which markets contribute the most revenue?
* How do delivery delays affect customer satisfaction?
* Where should the business focus its improvement efforts?

This project answers these questions by combining **Python, PostgreSQL, and Power BI** into a single analytical workflow.

---

## 🎯 Business Objectives

The analysis focuses on five major areas:

1. **Revenue & Sales Performance**
2. **Customer Segmentation & Retention**
3. **Product & Category Performance**
4. **Delivery & Customer Satisfaction**
5. **Geographic & Business Opportunity Analysis**

---

## 🗂️ Dataset

The project uses the **Olist Brazilian E-Commerce Public Dataset**, containing approximately 100K orders and multiple related datasets.

### Main datasets

* Customers
* Orders
* Order Items
* Payments
* Reviews
* Products
* Sellers
* Geolocation
* Product Category Translation

The dataset covers orders from approximately **2016–2018**.

---

## 🛠️ Tools & Technologies

| Tool       | Purpose                                |
| ---------- | -------------------------------------- |
| Python     | Data cleaning and exploratory analysis |
| Pandas     | Data manipulation                      |
| NumPy      | Numerical analysis                     |
| Matplotlib | Data visualization                     |
| PostgreSQL | SQL analytics and data modeling        |
| Power BI   | Interactive dashboard                  |
| DAX        | KPI calculations                       |
| GitHub     | Project documentation and portfolio    |

---

# 🔎 Analysis Performed

## 1. Revenue Analysis

Analyzed:

* Total revenue
* Monthly revenue trends
* Average Order Value
* Order volume
* Revenue concentration

### Key metrics

| Metric              |   Result |
| ------------------- | -------: |
| Total Orders        |   99,441 |
| Unique Customers    |   96,096 |
| Merchandise Revenue | R$13.59M |
| Average Order Value | R$136.68 |

---

## 2. Customer Intelligence

Customer analysis uses `customer_unique_id` to correctly identify customers across multiple orders.

### Customer Retention

The analysis found:

* **96,096 unique customers**
* **2,997 repeat customers**
* **3.12% repeat customer rate**

This indicates that customer retention represents a significant growth opportunity.

### RFM Analysis

Customers were segmented using:

* **Recency** — how recently they purchased
* **Frequency** — how often they purchased
* **Monetary** — how much they spent

Segments include:

* Champions
* Loyal Customers
* Potential Loyalists
* Needs Attention
* At Risk
* Lost Customers

---

## 3. Product & Category Analysis

Analyzed category-level:

* Revenue
* Units sold
* Average selling price
* Review scores
* Delivery performance

### Top revenue categories

1. Health & Beauty
2. Watches & Gifts
3. Bed & Bath Table
4. Sports & Leisure
5. Computers & Accessories

An important finding was that **sales volume does not always equal revenue contribution**. Some categories generate significantly higher revenue per unit because of higher average selling prices.

---

## 4. Delivery & Customer Satisfaction

Delivery performance was analyzed by comparing:

**Actual Delivery Date vs Estimated Delivery Date**

### Results

* On-time delivery: **93.23%**
* Late delivery: **6.77%**

The relationship between delivery and reviews was particularly significant:

| Delivery Status | Average Review |
| --------------- | -------------: |
| On Time         |       4.29 / 5 |
| Late            |       2.27 / 5 |

Late deliveries were therefore strongly associated with lower customer review scores.

> Note: This represents an association, not proof of causation.

---

## 5. Geographic Analysis

Revenue was analyzed across Brazilian states.

### Key finding

**São Paulo generated approximately 38.3% of merchandise revenue.**

São Paulo, Rio de Janeiro, and Minas Gerais together accounted for approximately **63.4% of revenue**.

The analysis also compared revenue per customer to identify smaller markets that may have attractive customer value.

---

# 📊 Power BI Dashboard

The Power BI dashboard contains four analytical pages.

### 1. Executive Overview

Includes:

* Revenue KPI
* Order KPI
* Customer KPI
* Average Order Value
* Monthly Revenue Trend
* Monthly Orders
* Revenue by Category
* Revenue by State

### 2. Customer Intelligence

Includes:

* Customer KPIs
* RFM Segmentation
* Revenue by Customer Segment
* One-Time vs Repeat Customers
* Cohort Retention
* Churn Risk

### 3. Product & Operations

Includes:

* Category Revenue
* Units Sold by Category
* Delivery Performance
* Review Score vs Delivery Status

### 4. Business Recommendations

Converts analytical findings into actionable business strategies covering:

* Customer retention
* Delivery optimization
* Geographic strategy
* Product/category prioritization

---

# 💡 Key Business Insights

### 1. Retention is a major opportunity

Only **3.12% of customers were repeat customers**, indicating substantial potential to increase customer lifetime value through retention strategies.

### 2. High-value customers deserve targeted attention

RFM analysis identifies Champions and Loyal Customers that contribute disproportionately to revenue relative to their customer share.

### 3. Delivery performance matters

Late deliveries were associated with an average review score of **2.27**, compared with **4.29** for on-time deliveries.

### 4. Revenue is geographically concentrated

São Paulo alone contributes approximately **38.3%** of merchandise revenue.

### 5. Category performance should be evaluated using multiple metrics

Revenue, units sold, average price, review score, and delivery performance provide a more complete picture than sales volume alone.

---

# 🚀 Business Recommendations

## Improve Customer Retention

* Target high-value one-time customers.
* Build personalized post-purchase campaigns.
* Use RFM segments for targeted marketing.
* Encourage second purchases through loyalty incentives.
* Recommend complementary products.

## Reduce Delivery Problems

* Monitor sellers with consistently high late-delivery rates.
* Improve delivery-date estimation.
* Prioritize high-volume categories with delivery problems.
* Monitor orders approaching their estimated delivery date.

## Protect Core Markets

* Maintain strong logistics coverage in major revenue markets.
* Ensure product availability in high-value states.
* Investigate smaller markets with high revenue per customer.

## Optimize Product Categories

* Protect inventory for high-revenue categories.
* Investigate categories combining high revenue with poor delivery performance.
* Use customer and product behavior to improve recommendations.

---

# 📁 Project Structure

```text
ecommerce-analyst/
│
├── data/
│   └── raw/
│       ├── customers.csv
│       ├── orders.csv
│       ├── order_items.csv
│       ├── payments.csv
│       ├── reviews.csv
│       ├── products.csv
│       ├── sellers.csv
│       ├── geolocation.csv
│       └── category_translation.csv
│
├── notebooks/
│   └── 01_data_quality.ipynb
│
├── sql/
│   ├── analysis/
│   └── views/
│
├── dashboard/
│   └── ecommerce_dashboard.pbix
│
└── README.md
```

---

# 🧠 Analytical Techniques

The project demonstrates practical application of:

* Data cleaning
* Exploratory Data Analysis
* Data aggregation
* Data joining and transformation
* Customer segmentation
* RFM analysis
* Cohort analysis
* Churn-risk classification
* Revenue analysis
* Geographic analysis
* Operational analysis
* KPI development
* Business opportunity scoring
* Dashboard development

---

# 📈 End-to-End Workflow

```text
Olist Dataset
      ↓
Python / Pandas
      ↓
Data Cleaning & EDA
      ↓
PostgreSQL
      ↓
Business SQL Analysis
      ↓
Analytical Views
      ↓
Power BI
      ↓
Interactive Dashboard
      ↓
Business Insights
      ↓
Recommendations
```

---

# 👨‍💻 Skills Demonstrated

**Technical Skills**

Python • Pandas • NumPy • Matplotlib • SQL • PostgreSQL • Power BI • DAX • Data Visualization

**Analytics Skills**

EDA • Customer Segmentation • RFM • Cohort Analysis • Retention Analysis • KPI Development • Business Analysis • Operational Analytics

---

# 📌 Conclusion

This project demonstrates how raw e-commerce transaction data can be transformed into actionable business intelligence.

Rather than focusing only on descriptive sales metrics, the analysis connects **customer behavior, revenue, products, geography, logistics, and customer satisfaction** to identify practical opportunities for business improvement.
