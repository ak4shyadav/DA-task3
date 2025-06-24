# DA-task3
# Task 3 – SQL Practice on Retail Orders Dataset

This project is part of my Data Analytics Internship task. The goal was to practice basic SQL queries using a retail dataset.

## 📊 About the Dataset

I used a sample Superstore dataset which contains information about customer orders like:
- Order date
- Region and state
- Product category
- Sales, profit, quantity
- Shipping details

The dataset is in CSV format and named `SampleSuperstore.csv`.

## 🔧 Tools Used

- DB Browser for SQLite
- You can also use MySQL or PostgreSQL if you prefer

## 🔍 What I Practiced

Here are some of the SQL operations I performed on this dataset:

- `SELECT` – to view all the data
- `WHERE` – to filter data based on conditions
- `ORDER BY` – to sort the results
- `GROUP BY` – to group data and apply functions like `SUM()` or `COUNT()`
- `JOIN` – to combine data (if needed for advanced practice)
- Used `LIMIT`, aliases, and date functions as well

## 🧪 Example Queries

```sql
-- View all records
SELECT * FROM orders;

-- Total sales by region
SELECT Region, SUM(Sales) FROM orders GROUP BY Region;

-- Top 5 products by profit
SELECT Product_Name, SUM(Profit) as Total_Profit 
FROM orders 
GROUP BY Product_Name 
ORDER BY Total_Profit DESC 
LIMIT 5;
