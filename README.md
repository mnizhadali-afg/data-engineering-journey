# My Data Engineering Learning Journey

Welcome to my personal knowledge base and project portfolio! This is where I'm documenting my progress, insights, and projects as I learn Data Engineering.

---

## 🚀 Recent Learnings: SQL Fundamentals

Today, I focused on understanding core SQL concepts crucial for data extraction and transformation.

### 💡 Key Concepts Covered:

* **SELECT Statements:** How to retrieve data from tables.
    * `SELECT column_name FROM table_name;`
    * `SELECT * FROM table_name;` (Be careful with `*` in production!)
* **WHERE Clause:** Filtering data based on conditions.
    * Example: `SELECT product_name FROM products WHERE price > 100;`
* **JOINs:** Combining data from multiple tables.
    * `INNER JOIN`: Returns only matching rows.
    * `LEFT JOIN`: Returns all rows from the left table, and matched rows from the right.
    * *Self-note:* Remember to always specify `ON` clause for JOINs!

### 💻 Code Snippets & Examples:

#### Example: Joining Customers and Orders Data

```sql
SELECT
    c.customer_id,
    c.customer_name,
    o.order_id,
    o.order_date,
    o.total_amount
FROM
    customers AS c
INNER JOIN
    orders AS o ON c.customer_id = o.customer_id
WHERE
    o.order_date >= '2023-01-01';
