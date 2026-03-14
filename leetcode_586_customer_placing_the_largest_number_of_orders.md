# LeetCode 586 - Customer Placing the Largest Number of Orders

## Problem
https://leetcode.com/problems/customer-placing-the-largest-number-of-orders/

## SQL Solution

```sql
SELECT customer_number
FROM Orders
GROUP BY customer_number
ORDER BY COUNT(*) DESC
LIMIT 1;
