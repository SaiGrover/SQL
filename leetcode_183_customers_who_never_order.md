# LeetCode 183 - Customers Who Never Order

## Problem
https://leetcode.com/problems/customers-who-never-order/

## SQL Solution

```sql
SELECT name AS Customers
FROM Customers
WHERE id NOT IN (
    SELECT customerId
    FROM Orders
);
