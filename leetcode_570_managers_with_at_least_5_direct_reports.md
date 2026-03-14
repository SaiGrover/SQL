# LeetCode 570 - Managers with at Least 5 Direct Reports

## Problem
https://leetcode.com/problems/managers-with-at-least-5-direct-reports/

## SQL Solution

```sql
SELECT name
FROM Employee
WHERE id IN (
    SELECT managerId
    FROM Employee
    GROUP BY managerId
    HAVING COUNT(managerId) >= 5
);
