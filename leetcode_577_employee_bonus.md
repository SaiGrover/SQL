# LeetCode 577 - Employee Bonus

## Problem
https://leetcode.com/problems/employee-bonus/

## SQL Solution

```sql
SELECT e.name, b.bonus
FROM Employee e
LEFT JOIN Bonus b 
ON b.empId = e.empId
WHERE b.bonus IS NULL OR b.bonus < 1000;
