# SQL-Advance-ASSIGNMENTS
<div align="center">

# 🗄️ SQL Advanced Assignment
### Advanced SQL Queries, Window Functions, CTEs & Aggregations

<img src="https://img.shields.io/badge/SQL-Advanced-blue?style=for-the-badge&logo=mysql">
<img src="https://img.shields.io/badge/Queries-25-green?style=for-the-badge">
<img src="https://img.shields.io/badge/Level-Intermediate%20to%20Advanced-orange?style=for-the-badge">

</div>

---

# 📌 Overview

This repository contains solutions for an **Advanced SQL Assignment** covering:

- 🔹 Joins & Aggregations
- 🔹 Subqueries
- 🔹 Correlated Queries
- 🔹 Window Functions
- 🔹 Common Table Expressions (CTEs)
- 🔹 CASE Statements
- 🔹 Ranking & Analytical Queries

The assignment demonstrates practical database querying techniques using real-world business scenarios such as:

✔ Customer Spending Analysis  
✔ Revenue Calculation  
✔ Product Ranking  
✔ Sales Growth Analysis  
✔ Loyalty Classification  

---

# 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| MySQL | Database Management |
| SQL | Query Language |
| MySQL Workbench | Query Execution |
| GitHub | Version Control |

---

# 📂 Assignment Sections

## 🔹 A. Advanced Joins & Aggregations

<details>
<summary>Click to Expand</summary>

### Queries Included

1. Find total revenue collected by each shipper  
2. Top 5 highest-spending customers  
3. Product categories with average selling price > 8000  
4. Total orders per city  
5. Suppliers supplying multiple categories  
6. Orders with total item count  

</details>

---

## 🔹 B. Subqueries – Nested & Correlated

<details>
<summary>Click to Expand</summary>

### Queries Included

7. Customers spending above average  
8. Products priced above category average  
9. Customers with orders above ₹50,000  
10. Customers with above-average order count  
11. Most expensive products  

</details>

---

## 🔹 C. Window Functions

<details>
<summary>Click to Expand</summary>

### Queries Included

12. Rank customers based on spending  
13. Cumulative sales by order date  
14. Percentage contribution of customers  
15. Most recent order per customer  
16. Product ranking within categories  

</details>

---

## 🔹 D. CTE & CASE

<details>
<summary>Click to Expand</summary>

### Queries Included

17. Product price categorization using CASE  
18. Top 3 customers using CTE  
19. Customer loyalty classification  
20. Monthly revenue growth percentage  
21. Top 2 customers per city  

</details>

---

## 🔹 E. Miscellaneous Advanced Queries

<details>
<summary>Click to Expand</summary>

### Queries Included

22. Top cities with highest sales revenue  
23. Complete order details with supplier & shipper  
24. Total sales per supplier with average order value  
25. Product categories contributing more than 30% revenue  

</details>

---

# 📊 Sample SQL Query

```sql
SELECT Customers.customer_id,
       Customers.name,
       SUM(Order_Items.quantity * Order_Items.price_each) AS total_spent
FROM Customers
JOIN Orders 
    ON Customers.customer_id = Orders.customer_id
JOIN Order_Items 
    ON Orders.order_id = Order_Items.order_id
GROUP BY Customers.customer_id, Customers.name
ORDER BY total_spent DESC
LIMIT 5;
