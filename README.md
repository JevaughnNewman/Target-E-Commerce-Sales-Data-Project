# Table of Contents

- [Target E-commerce Analysis](#target-e-commerce-analysis)
  
  - [Executive Summary](#executive-summary)
  - [Project Background](#project-background)
  - [Insights and Deep-Dive](#insights-and-deep-dive)
    - [Sales Trends and Growth Rates](#sales-trends-and-growth-rates)
    - [Key Performance Indicators](#key-performance-indicators)
    - [Sales by Product Category](#sales-by-product-category)
    - [Payment Preference](#payment-preference)
    - [Customer Spend Category](#customer-spend-category)
  - [Recommendations](#recommendations)
  - [Clarifying Questions, Assumptions and Caveats](#clarifying-questions-assumptions-and-caveats)
    - [Questions for Stakeholders Before Project Advancement](#questions-for-stakeholders-before-project-advancement)
    - [Assumptions and Caveats](#assumptions-and-caveats)


# Executive Summary

<img width="1080" alt="Dashboard.png" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/611b4bf7891fb658210bb5fcefae037d052b0727/Dashboard.png">

### Overview of Findings

1. **YoY Revenue Growth**: In 2018, revenue grew to $7,386,050, marking a 19.99% year-over-year increase. This growth was driven by a 20.4% rise in order volume, from 13,948 in 2017 to 16,794 in 2018. Notably, customers in the high-spender category, defined by the percentile of average cart amount, contributed to this upward trend with increases in both revenue and order quantity. However, the average order value (AOV) for this segment saw a slight decline, dropping from $299.07 to $295.22.

2. **Top-Selling Product Categories**:  
   In 2017, the leading product categories by revenue were Bed, Bath & Tableware, Watches & Accessories, Health & Beauty, Sports & Leisure, and Computer & Laptop Accessories. These top 5 categories collectively contributed to 37.8% of the total revenue for the year.  

   When comparing 2018, the same five categories continued to dominate in terms of overall revenue. However, the share of total revenue from these top categories increased to 41.3% in the first three quarters of 2018.


# Project Background

Target is a leading retail company in the United States, known for its wide array of products, including clothing, electronics, groceries, and household items. To enhance its customer experience and expand its global presence, Target has invested heavily in its international e-commerce operations, allowing customers in various regions to browse, purchase, and receive products conveniently through online orders.

This project focuses on analyzing e-commerce sales data from Target’s international operations in Brazil to assess key sales performance trends, product performance, and customer behavior. By leveraging this data, we aim to uncover insights that can inform business strategies and operational improvements.

Key areas of analysis include:

1) Sales Performance

2) Customer Behaviour

3) Product Performance

① The interactive Tableau Dashboard can be accessed [HERE](https://public.tableau.com/app/profile/jevaughn.newman/viz/TargetEcommerceDashboard/ExecutiveDashboard?publish=yes)

② The executive slide deck for the strategic growth strategy based on the insights we uncovered [View Presentation](./public/Brazil_E-Commerce_Accelerated_Growth_Strategy.pdf](https://github.com/JevaughnNewman/portfolio/blob/main/public/Brazil_E-Commerce_Accelerated_Growth_Strategy.pdf)

③ The queries used to create the relational database in MySQL Workbench 8.0.40 Community can be found [HERE](https://docs.google.com/document/d/1DeTPUa9PTz7XdSBD7RKVmE9SlXT6voAUoSrybSxRRg4/edit?tab=t.44mx9ut4pvzc)


# Data Structure & Initial Checks

The Target E-commerce Sales database structure consists of seven tables: Orders, Order_Items, Products, Payments, Customers, Sellers, and Geolocation

Each table has a total row count of approximately 100,000 records.

<img width="1080" alt="Target E-Commerce ERD Diagram.png" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/ea6b579a2aa48e692d81179ea4248955bd4c84ea/Target%20E-Commerce%20ERD%20Diagram.png">



Fact Table: 

    Order_items Description: This table captures detailed transactional data for each item in an order. It serves as the central fact table for our analysis
  
    Key Columns: 
    
    - order_item_id: Unique identifier (Primary Key) for each item in an order.
    
    - order_id: Links the item to the corresponding order.
    
    - product_id: Identifies the product sold.
    
    - price: The price of the item.
    
    - freight_value: shipping cost for the item.

Dimension Tables: 

    Orders: This section tracks order lifecycle timelines (purchase, delivery, and estimates) and statuses, which are linked to customers.
    
    - Products: Manages product metadata, including category, dimensions, and descriptive content for inventory and logistics.
    
    - Payments: Logs payment methods, installments, and transaction values tied to orders for financial reporting.
    
    - Customers: Stores unique customer profiles with ZIP code-linked location data for delivery and analysis.
    
    Sellers: This section contains seller details, including location via ZIP code, to track seller geographic distribution and performance.
    
    - Geolocation: Central table storing geographic coordinates and city/state data for ZIP code prefixes used by customers and sellers.
      

# Insights and Deep Dive

### Sales Trends and Growth Rates

- **Year-Over-Year (YoY) Revenue Growth**:  
  Revenue grew from **$6,155,806.98 in 2017** to **$7,386,050 in 2018**, marking a **19.99% increase**. However, it's important to note that the 2018 data includes only the first three quarters.  

- **Average Order Value (AOV)**:  
  The **AOV in 2017 was $138.09**, while in **2018 it slightly declined to $137.35**. Despite the drop in AOV, the **overall order volume increased by 20.4%**, contributing to the YoY revenue growth.  

- **Growth in High-Spend Customers**:  
  Customers classified as **high spenders** made up a **larger percentage of overall orders in 2018 compared to 2017**. These high-spending customers predominantly purchased from the **top five product categories**, reinforcing the importance of these key segments.  

- **2017 Revenue Growth and Q4 Peak**:  
  In **2017, revenue steadily increased from Q1 to Q4**, with a peak in **November 2017 at $1,010,271**, most likely driven by holiday shopping for **Christmas**.  

- **Top Revenue-Generating Categories in Holiday Season (Q4 2017)**:  
  During the **holiday season (Q4 2017), the categories that contributed the most revenue were**:  
  - **Watches & Accessories**  
  - **Bed, Bath & Tableware**  
  - **Health & Beauty**  
  - **Sports & Leisure**  
  - **Toys & Games**  

### Key Performance Indicators

- **Year-over-Year Revenue Growth**: Revenue saw a notable increase of **19.99%** YoY, rising from **$6,155,806.98 in 2017** to **$7,386,050 in 2018**. It's important to note that the 2018 metric only includes data for the first three quarters, which highlights significant growth despite the incomplete data for the full year.

- **Average Order Value (AOV)**: The average order value slightly decreased from **$138.09 in 2017** to **$137.35 in 2018**, indicating a marginal reduction in spending per transaction, which could be attributed to shifts in customer behavior or product mix.

- **Top 5 Product Categories by Revenue**: The following product categories were the largest contributors to revenue:
  - **Bed, Bath & Tableware**
  - **Watches & Accessories**
  - **Health & Beauty**
  - **Sports & Leisure**
  - **Computer & Laptop Accessories**

  These top 5 categories accounted for **37.8% of total revenue in 2017** and **41.3% in the first three quarters of 2018**, underscoring their strong performance and consistent demand.

### Sales by Product Category

  * In both 2017 and 2018, revenue was heavily concentrated in a few key product categories. The top five **Bed, Bath & Tableware, Watches & Accessories, Health & Beauty, Sports & Leisure, and Computer & Laptop Accessories** accounted for **37.8% of total revenue in 2017** and increased their share to **41.3% in 2018**. The **high-spending customer segment** made up the largest percentage of sales and showed a strong preference for these top categories, further driving revenue growth in 2018.  

  * Seasonal trends played a significant role in category performance, with **Q4 of 2017 experiencing the highest revenue peak**, culminating in **November's total revenue of $1,010,271**, likely due to increased **holiday shopping activity**. During this period, **Watches & Accessories, Bed, Bath & Tableware, Health & Beauty, Sports & Leisure, and Toys & Games** generated the largest portion of revenue. This trend underscores the impact of seasonal demand on product category performance, particularly during the holiday season.  

  * While the top categories remained dominant, **some segments experienced shifts in demand**. **Electronics growth slowed**, possibly indicating **market saturation or increased competition**, while **mid-tier customers drove sales in Health & Beauty and Sports & Leisure**. The increase in revenue share from high-spending customers suggests **a greater concentration of purchases among premium buyers**, reinforcing the need to tailor product offerings and marketing strategies to high-value segments.  

### Payment Preference

<p align="center">
<img width="600" alt="PaymentMethods.png" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/e0db4600d80036b7aefc12fce017153d1e15b6ba/PaymentMethod.png">
</p>

  * Payment Preferences by Customer Spend Category: Credit cards and UPI (Unified Payments Interface) dominate as the preferred payment methods across all customer spend categories, accounting for approximately 96.44% of all transactions. Among these, credit cards remain the most widely used payment method, with customers consistently opting for this method for higher-value orders.
    
  * Unified Payments Interface (UPI): UPI, also known as PIX in Brazil, is a real-time payment system introduced by the Central Bank of Brazil (Banco Central do Brasil) in 2020. It allows users to make instant, secure payments around the clock, including weekends and holidays, at no cost. UPI has quickly gained traction, accounting for 19.29% of total transactions. The system enables quick and easy payments, often facilitated through QR code scanning, making it an attractive alternative for consumers.
    
  * It may be beneficial for Target Brazil to incentivize customers to utilize PIX more regularly due to the lower transaction fees compared to credit card payments. In addition to this, the speed and security of UPI may allow our customers to purchase more often.


### Customer Spend Category


#### High Spenders

<p align="center">
<img width="1080" alt="HighSpenderKPIs.png" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/68f36115065c7a1b457259894d37760ddacef539/High%20Spender%20KPI%202017.png">
</p>

  * In 2017, customers categorized as high spenders placed a total of 13,948 orders, with an average order value (AOV) of $299.07, generating $4,171,469.07 in total revenue. This segment accounted for a 21.9% share of total revenue for the year.
  * the top spend categories for customers categorized as low spenders were: Watches & Accessories, Bed, Bath & Tableware, Health & Beauty, Sports & Leisure and Computers & Laptop Accessories.

<p align="center">
<img width="1080" alt="HighSpenderKPIs.png" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/68f36115065c7a1b457259894d37760ddacef539/High%20Spender%20KPI%202018.png">
</p>

  * In 2018, the total number of orders increased by 20.4%, rising from 13,948 to 16,794 orders. While the AOV slightly decreased from $299.07 to $295.22, the overall revenue for this customer segment grew 18.85% YoY, reaching $4,957,959.75. The high spender segment represented a larger share of total revenue in 2018, reinforcing its importance to overall business growth.

#### Medium Spenders

* In 2017, customers categorized as medium spenders made a total of 17,927 orders, generating a revenue of $1,572,786.69. The average order value (AOV) for this segment was $87.73.

<p align="center">
<img width="1080" alt="MediumSpenderKPIs.png" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/676c2172b94ce36fa6fcdcc48cf0ab472ba193e7/Medium%20Spender%20KPI%202018.png">
</p>

* In 2018, the total quantity of orders increased by 17.97%, rising from 17,927 to 21,079 orders. This increase in order quantity was accompanied by a 3.20% increase in AOV, which rose from $87.73 in 2017 to $90.53 in 2018. As a result, the total revenue from medium spend customers increased by 21.33%, reaching $1,908,311.48 in 2018.

#### Low Spenders

  * In 2017, customers whose average order size was categorized as low spenders made a total of 12,703 orders. The average order value (AOV) for customers in the low spender category was $32.40, and the revenue totalled $411,551.22.
  * the top spend categories for customers categorized as low spenders were: home decor, cell phones & accessories, Computer and laptop accessories, Bed, bath & tableware, and sports & leisure.
  * Customers in the low spend category represented 6.7% of total revenue for 2017.

<p align="center">
<img width="1080" alt="LowSpenderKPIs.png" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/c492aea0e4ba9d4687c4c4e18929c7475a6aee6b/Low%20Spender%20KPI%202018.png">
</p>

    
  * In 2018, the total quantity of orders for customers in this category increased 25.18% from 12,703 to 15,902, accompanied by a slight increase in the average order value (AOV), which increased from $32.69 to a previous average order value of $32.40. Total YoY% revenue for this customer profile increased to $519,779.57, which represented a 26.30% increase from 2017's revenue of $411,551.22.

    


# Recommendations

 1. **Payment Methods**: Incentivize UPI Adoption to Reduce Merchant Fees and Enhance Payment Efficiency
    
    * Lower Merchant Fees: UPI transactions have significantly lower or no fees compared to credit card payments, which can reduce overall transaction costs for the business.
    * Offer discounts, cashback, or loyalty rewards for customers who use UPI to increase its share from the current 19.29% of total transactions.
    * Educate customers on the security, speed, and convenience of UPI to drive long-term adoption.

 2. **Optimize Product Category Strategy for Seasonal Demand**: 

    * Leverage Q4 sales peaks by enhancing promotions and stock levels in Watches & Accessories, Bed, Bath & Tableware, Health & Beauty, Sports & Leisure, and Toys & Games, which performed best during the holiday season.
    * Expand product bundling and upsell strategies in top-selling categories to increase Average Order Value (AOV).
    * Use historical sales data to improve inventory planning and tailor marketing campaigns to maximize peak-season revenue.

 3. **Capitalize on High-Spending Customer Trends**: 

    * The high-spender segment is growing as a percentage of total orders and prefers the top revenue-generating categories.
    * Develop exclusive VIP programs, premium-tier discounts, and early-access sales for high-value customers to boost retention and revenue.
    * Use personalized promotions and targeted marketing based on past purchase behavior to maximize customer lifetime value.

 4. **Expand Focus on Mid-Tier Customers for Long-Term Growth**: 

    * While high spenders dominate revenue, mid-tier customers drove increased sales in Health & Beauty and Sports & Leisure, offering an opportunity for targeted growth.
    * Introduce flexible payment plans, loyalty incentives, and personalized promotions to encourage repeat purchases from this segment.
  
     
# Clarifying Questions, Assumptions and Caveats

### Questions for Stakeholders Before Project Advancement
1. What are the key business objectives this analysis should address?

   * Answer: Identify revenue trends, customer behaviour and the highest selling product categories

3. What data sources are available, and do we have full access to them?

   * Answer: Product sales data from Target’s international operations in Brazil. The dataset does not include specific product names or customer names to protect privacy. It covers Q4 2016, all of 2017, and Q1–Q3 of 2018.
   
5. Who is the primary audience for this analysis, and how will insights be used?

   * Answer: Executives and marketing teams. Insights will guide pricing, marketing, and inventory decisions.

### Assumptions and Caveats

#### Assumptions
- The provided dataset is **complete and accurate**, representing all transactions from the specified periods.  
- The **absence of specific product names and customer names** does not significantly impact the validity of customer behavior insights.  
- Sales trends from **Target’s international operations in Brazil** are reflective of broader e-commerce trends in that market.  

#### Caveats
- The dataset **only includes Q4 2016, all of 2017, and Q1–Q3 of 2018**, meaning **Q4 2018 is missing**, which may affect year-over-year comparisons.  
- Without customer-specific data:
  - **Repeat purchase behavior cannot be directly measured** and must be inferred from transaction details.  
  - **Customer segmentation is limited** to spending patterns rather than demographics.  
- **Macroeconomic factors** (e.g., inflation, currency fluctuations) that could impact purchasing behavior are **not accounted for** in this analysis.  





