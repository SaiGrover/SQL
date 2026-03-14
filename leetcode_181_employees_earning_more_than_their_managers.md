# LeetCode 181 - Employees Earning More Than Their Managers

## Problem
https://leetcode.com/problems/employees-earning-more-than-their-managers/

## SQL Solution

```sql
WITH salaries AS (
    SELECT id, name, salary, managerId
    FROM Employee
)

SELECT e.name AS Employee
FROM salaries e
JOIN salaries m
    ON e.managerId = m.id
WHERE e.salary > m.salary;
