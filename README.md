# Customer Shopping Behavior Analysis

## 📌 Project Overview
This project analyzes customer shopping behavior using transactional data from 3,900 purchases across various product categories. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior to guide strategic business decisions.

---

## 📊 Dataset Summary
* **Total Rows:** 3,900
* **Total Columns:** 18
* **Customer Demographics:** Age, Gender, Location, Subscription Status.
* **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color.
* **Shopping Behavior:** Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type.
* **Missing Data:** 37 missing values were identified in the Review Rating column.

---

## 🛠️ Data Preparation & Exploratory Data Analysis (Python)
Data was initially loaded, cleaned, and explored using Python (pandas):

* **Initial Exploration:** Used `df.info()` to check the data structure and `describe()` for summary statistics.
* **Handling Missing Data:** Imputed missing values in the Review Rating column using the median rating of each product category.
* **Standardization:** Renamed columns to snake_case for better readability and documentation.
* **Feature Engineering:** Created an `age_group` column by binning customer ages and a `purchase_frequency_days` column from the purchase data.
* **Data Consistency:** Dropped the `promo_code_used` column after verifying it was redundant with `discount_applied`.
* **Database Integration:** The cleaned DataFrame was loaded into PostgreSQL for structured SQL analysis.

---

## 🔍 Key Insights & SQL Analysis
Structured queries in PostgreSQL revealed several core business insights:

* **Revenue by Gender:** Male customers generated the majority of the revenue at $157,890, compared to $75,191 from Female customers.
* **Top Products by Rating:** The highest-rated products on average were Gloves (3.86), Sandals (3.84), and Boots (3.82).
* **Shipping & Spend:** Purchases using Express shipping averaged slightly higher ($60.48) than those using Standard shipping ($58.46).
* **Customer Segmentation:** Based on purchase history, customers were segmented into Loyal (3,116), Returning (701), and New (83).
* **Revenue by Age Group:** The Young Adult segment contributed the most total revenue ($62,143), followed by Middle-aged ($59,197), Adult ($55,978), and Senior ($55,763).
* **Subscription Impact:** 1,053 customers are subscribers generating $62,645, while 2,847 non-subscribers generate $170,436.

---

## 📈 Power BI Dashboard
An interactive dashboard was built in Power BI to present these insights visually. Key top-line metrics displayed on the dashboard include:

* **Total Customers:** 3.9K
* **Average Purchase Amount:** $59.76
* **Average Review Rating:** 3.75
* **Subscriber Ratio:** 27% of customers are subscribed, while 73% are not.

---

## 💡 Business Recommendations
Based on the analysis, the following strategic actions are recommended:

* **Boost Subscriptions:** Promote exclusive benefits for subscribers to increase the subscriber base.
* **Customer Loyalty Programs:** Reward repeat buyers to encourage them to move into the "Loyal" segment.
* **Review Discount Policy:** Strategically balance sales boosts from discounts with profit margin control.
* **Product Positioning:** Highlight top-rated and best-selling products in future marketing campaigns.
* **Targeted Marketing:** Focus marketing efforts on high-revenue demographics (like Young Adults) and express-shipping users.
