# LeetCode 1070 - Product Sales Analysis III

## Problem
https://leetcode.com/problems/product-sales-analysis-iii/

## SQL Solution

```sql
WITH first_year_cte AS (
    SELECT product_id, MIN(year) AS first_year
    FROM Sales
    GROUP BY product_id
)

SELECT s.product_id, s.year AS first_year, s.quantity, s.price
FROM Sales s
JOIN first_year_cte f
ON s.product_id = f.product_id
AND s.year = f.first_year;
```
