# LeetCode 584 - Find Customer Referee

## Problem
https://leetcode.com/problems/find-customer-referee/

## SQL Solution

```sql
SELECT c.name
FROM Customer c
WHERE referee_id IS NULL 
   OR referee_id != 2;
