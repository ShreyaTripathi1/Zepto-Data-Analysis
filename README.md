# Zepto-Data-Analysis

## Overview

This project involves the analysis of an e-commerce inventory dataset scraped from Zepto, one of India’s fastest-growing quick-commerce startups. The dataset is used to create a database table, perform data exploration, cleaning, and analysis to derive meaningful insights about product inventory, pricing, and categories.

## Dataset:
The dataset is sourced from Kaggle: Zepto Inventory Dataset.
E-commerce inventory dataset scraped from Zepto — one of India’s fastest-growing quick-commerce startups.

Link : https://www.kaggle.com/datasets/palvinder2006/zepto-inventory-dataset/data?select=zepto_v2.csv

## SQL Components

**1. Table Creation**
The zepto table is created with the following schema:

- ```sku_id```: Serial primary key
- ```category```: Product category (VARCHAR)
- ```name```: Product name (VARCHAR, NOT NULL)
- ```mrp```: Maximum retail price (NUMERIC)
- ```discountPercent```: Discount percentage (NUMERIC)
- ```availableQuantity```: Stock quantity (INTEGER)
- ```discountedSellingPrice```: Selling price after discount (NUMERIC)
- ```weightInGms```: Product weight in grams (INTEGER)
- ```outOfStock```: Stock status (BOOLEAN)
- ```quantity```: Quantity field (INTEGER)

**2. Data Exploration**
The following queries are used to explore the dataset:
- Count total rows in the table.
- Retrieve a sample of 10 records.
- Check for null values across columns.
- List distinct product categories.
- Count products that are in/out of stock.
- Identify products with multiple SKUs.

**3. Data Cleaning**
The cleaning process includes:
- Identifying and deleting products with an MRP or discounted selling price of 0.
- Converting prices from paise to rupees by dividing mrp and discountedSellingPrice by 100.

**4. Data Analysis**
The following analytical queries are performed:

**_Top 10 Best-Value Products_**: Based on discount percentage.

**_High MRP Out-of-Stock Products_**: Products with MRP > ₹300 and out of stock.

**_Estimated Revenue by Category_**: Sum of discountedSellingPrice * availableQuantity per category.

**_High MRP Low Discount Products_**: Products with MRP > ₹500 and discount < 10%.

**_Top 5 Categories by Average Discount_**: Categories with the highest average discount percentage.

**_Price Per Gram_**: For products weighing ≥100g, sorted by best value.

**_Weight-Based Categorization_**: Products grouped into Low (<1000g), Medium (<5000g), or Bulk (≥5000g) categories.

**_Total Inventory Weight by Category_**: Sum of weightInGms * availableQuantity per category.
