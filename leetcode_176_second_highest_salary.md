# LeetCode 176 - Second Highest Salary

## Problem
https://leetcode.com/problems/second-highest-salary/

## SQL Solution

```sql
SELECT (
    SELECT DISTINCT salary
    FROM Employee
    ORDER BY salary DESC
    LIMIT 1 OFFSET 1
) AS SecondHighestSalary;
