# Project Background

Target is a leading retail company in the United States, known for its wide array of products, including clothing, electronics, groceries and household items. To enhance its customer experience and expand its reach worldwide, Target has invested heavily in its e-commerce platform, which enables customers to browse, purchase and receive products conveniently through online orders.

This project focuses on utilizing the e-commerce data to perform key sales and product performance analyses and give customer insights.

Insights and recommendations are provided in the following key areas:




# Data Structure & Initial Checks

The Target E-commerce Sales database structure consists of seven tables: Orders, Order_Items, Products, Payments, Customers, Sellers, Geolocation

Each table has a total row count of approximately 100,000 records.

<img width="1080" alt="Target ERD Diagram" src="https://github.com/JevaughnNewman/Target-E-Commerce-Sales-Data-Project/blob/52db85a0e08683a076ff188a6593d4d4ef174f9d/Target%20ERD%20Diagram.png">



Fact Table: Order_items
    - **Description: This table captures detailed transactional data for each item in an order. It serves as the central fact table for our analysis
  
  Key Columns: 
    - **order_item_id: Unique identifier (Primary Key) for each item in an order
    - ** order_id: Links the item to the corresponding order.
    - **product_id: Identifies the product sold.
    - **price: The price of the item.
    - **freight_value: shipping cost for the item.

Dimension Tables: 
  Orders: 
  Products: 
  Payments: 
  Customers: 
  Sellers:
  Geolocation:



# Executive Summary




# Insights and Deep Dive
