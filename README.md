# Table of Contents

- [Target E-commerce Analysis](#target-e-commerce-analysis)
  
  - [Project Background](#project-background)
  - [Executive Summary](#executive-summary)
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


# Project Background

Target is a leading retail company in the United States, known for its wide array of products, including clothing, electronics, groceries, and household items. To enhance its customer experience and expand its global presence, Target has invested heavily in its international e-commerce operations, allowing customers in various regions to browse, purchase, and receive products conveniently through online orders.

This project focuses on analyzing e-commerce sales data from Target’s international operations in Brazil to assess key sales performance trends, product performance, and customer behavior. By leveraging this data, we aim to uncover insights that can inform business strategies and operational improvements.

Key areas of analysis include:

1) Sales Performance

2) Customer Behaviour

3) Product Performance 


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

    Orders: This section tracks order lifecycle timelines (purchase, delivery, estimates) and statuses, which are linked to customers.
    
    - Products: Manages product metadata, including category, dimensions, and descriptive content for inventory and logistics.
    
    - Payments: Logs payment methods, installments, and transaction values tied to orders for financial reporting.
    
    - Customers: Stores unique customer profiles with ZIP code-linked location data for delivery and analysis.
    
    Sellers: This section contains seller details, including location via ZIP code, to track seller geographic distribution and performance.
    
    - Geolocation: Central table storing geographic coordinates and city/state data for ZIP code prefixes used by customers and sellers.



# Executive Summary

<img width="1080" alt="Dashboard.png" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/611b4bf7891fb658210bb5fcefae037d052b0727/Dashboard.png">

### Overview of Findings

1. **YoY Revenue Growth**: In 2018, revenue grew to $7,386,050, marking a 19.99% year-over-year increase. This growth was driven by a 20.4% rise in order volume, from 13,948 in 2017 to 16,794 in 2018. Notably, customers in the high-spender category, defined by the percentile of average cart amount, contributed to this upward trend with increases in both revenue and order quantity. However, the average order value (AOV) for this segment saw a slight decline, dropping from $299.07 to $295.22.

2. **Top-Selling Product Categories**:  
   In 2017, the leading product categories by revenue were Bed, Bath & Tableware, Watches & Accessories, Health & Beauty, Sports & Leisure, and Computer & Laptop Accessories. These top 5 categories collectively contributed to 37.8% of the total revenue for the year.  

   When comparing 2018, the same five categories continued to dominate in terms of overall revenue. However, the share of total revenue from these top categories increased to 41.3% in the first three quarters of 2018.

      



# Insights and Deep Dive

### Sales Trends and Growth Rates


### Key Performance Indicators


### Sales by Product Category


### Payment Preference

<img width="720" alt="PaymentMethods.png" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/e0db4600d80036b7aefc12fce017153d1e15b6ba/PaymentMethod.png">


  * Payment Preferences by Customer Spend Category: Credit cards and UPI (Unified Payments Interface) dominate as the preferred payment methods across all customer spend categories, accounting for approximately 96.44% of all transactions. Among these, credit cards remain the most widely used payment method, with customers consistently opting for this method for higher-value orders.
    
  * Unified Payments Interface (UPI): UPI, also known as PIX in Brazil, is a real-time payment system introduced by the Central Bank of Brazil (Banco Central do Brasil) in 2020. It allows users to make instant, secure payments around the clock, including weekends and holidays, at no cost. UPI has quickly gained traction, accounting for 19.29% of total transactions. The system enables quick and easy payments, often facilitated through QR code scanning, making it an attractive alternative for consumers.
    
  * It may be beneficial for Target Brazil to incentivize customers to utilize PIX more regularly due to the lower transaction fees compared to credit card payments. In addition to this, the speed and security of UPI may allow our customers to purchase more often.


### Customer Spend Category
  * In 2017, customers whose average order size was categorized as low spenders made a total of 12,703 orders. The average order value (AOV) for customers in the low spender category was $32.40, and the revenue totalled $411,551.22.
  * the top spend categories for customers categorized as low spenders were: home decor, cell phones & accessories, Computer and laptop accessories, Bed, bath & tableware, and sports & leisure.
  * Customers in the low spend category represented 6.7% of total revenue for 2017.
    
  * In 2018, the total quantity of orders for customers in this category increased 25.18% from 12,703 to 15,902, accompanied by a slight increase in the average order value (AOV), which increased from $32.69 to a previous average order value of $32.40. Total YoY% revenue for this customer profile increased to $519,779.57, which represented a 26.30% increase from 2017's revenue of $411,551.22.

    


# Recommendations

 **Payment Methods**: Incentivize UPI Adoption to Reduce Merchant Fees and Enhance Payment Efficiency
    
  1. Lower Merchant Fees: UPI transactions have significantly lower or no fees compared to credit card payments, which can reduce overall transaction costs for the business.
  2. Faster, Secure Payments: UPI offers instant, 24/7 payments with enhanced security, providing a seamless and reliable payment experience for customers.
  3. Customer Convenience and Loyalty: Promoting UPI simplifies the payment process for customers and incentivizing its use can enhance customer loyalty through rewards, fostering repeat business.




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





