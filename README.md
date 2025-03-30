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

Target is a leading retail company in the United States, known for its wide array of products, including clothing, electronics, groceries and household items. To enhance its customer experience and expand its reach worldwide, Target has invested heavily in its e-commerce platform, which enables customers to browse, purchase and receive products conveniently through online orders.

This project focuses on utilizing the e-commerce data to perform key sales and product performance analyses and give customer insights.

Insights and recommendations are provided in the following key areas:

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

**Overview of Findings**

1. YoY revenue Growth: In 2018, revenue grew to $7,386,050, marking a 19.99% year-over-year increase. This growth was driven by a 20.4% rise in order volume, from 13,948 in 2017 to 16,794 in 2018. Notably, customers in the high-spender category, defined by the percentile of average cart amount, contributed to this upward trend with increases in both revenue and order quantity. However, the average order value (AOV) for this segment saw a slight decline, dropping from $299.07 to $295.22.
    
2. Changes in Top-Selling Product Categories: 
    



# Insights and Deep Dive

### Sales Trends and Growth Rates


### Key Performance Indicators


### Sales by Product Category


### Payment Preference


### Customer Spend Category


# Recommendations

# Clarifying Questions, Assumptions and Caveats

## Questions for Stakeholders Before Project Advancement
List of key questions for stakeholders before moving forward with the project...

## Assumptions and Caveats
Details about assumptions made in the analysis and any potential caveats...





