# LeetCode 607 - Sales Person

## Problem
https://leetcode.com/problems/sales-person/

## SQL Solution

```sql
SELECT name
FROM SalesPerson
WHERE sales_id NOT IN (
    SELECT sales_id
    FROM Company
    INNER JOIN Orders
        ON Company.com_id = Orders.com_id
    WHERE Company.name = 'RED'
);
