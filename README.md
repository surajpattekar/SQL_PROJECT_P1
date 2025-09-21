# 🛍️ Retail Sales Analysis (SQL Project)

## 📌 Introduction
Retail businesses generate thousands of transactions every day.  
This project is an **end-to-end SQL case study** analyzing a retail sales dataset to extract insights about:
- Sales trends  
- Customer behavior  
- Product category performance  
- Best-selling periods  
- Top customers  

---

## 🎯 Problem Statement
The company wants to answer:
1. How many sales and unique customers do we have?  
2. Which categories are performing the best?  
3. What is the average age of Beauty buyers?  
4. Which months generate the highest sales?  
5. Who are our top customers?  
6. How do sales differ by time of day (morning/afternoon/evening)?  

---

## 📊 Dataset
The dataset contains **retail transactions** with the following fields:

| Column          | Description                         |
|-----------------|-------------------------------------|
| transaction_id  | Unique ID of each sale              |
| sale_date       | Date of transaction                 |
| sale_time       | Time of transaction                 |
| customer_id     | Unique customer ID                  |
| gender          | Gender of customer                  |
| age             | Age of customer                     |
| category        | Product category (Clothing, Beauty, Electronics, etc.) |
| quantity        | Quantity sold                       |
| price_per_unit  | Unit price of product               |
| cogs            | Cost of goods sold                  |
| total_sale      | Total sales value (quantity × price)|

---

## 🧹 Data Cleaning
```sql
-- Find NULL values
SELECT * FROM retail_sales
WHERE transaction_id IS NULL
   OR sale_date IS NULL
   OR sale_time IS NULL
   OR gender IS NULL
   OR category IS NULL
   OR quantity IS NULL
   OR cogs IS NULL
   OR total_sale IS NULL;

-- Remove NULL records
DELETE FROM retail_sales
WHERE transaction_id IS NULL
   OR sale_date IS NULL
   OR sale_time IS NULL
   OR gender IS NULL
   OR category IS NULL
   OR quantity IS NULL
   OR cogs IS NULL
   OR total_sale IS NULL;
