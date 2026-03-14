# LeetCode 1068 - Product Sales Analysis I

## Problem
https://leetcode.com/problems/product-sales-analysis-i/

## SQL Solution

```sql
SELECT p.product_name, s.year, s.price
FROM Sales s
LEFT JOIN Product p
ON p.product_id = s.product_id;
```
