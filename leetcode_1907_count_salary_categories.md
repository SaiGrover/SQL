# LeetCode 1907 - Count Salary Categories

## Problem
https://leetcode.com/problems/count-salary-categories/

## SQL Solution

```sql
WITH all_categories AS (
    SELECT 'Low Salary' AS category
    UNION ALL
    SELECT 'Average Salary'
    UNION ALL
    SELECT 'High Salary'
),
category_count AS (
    SELECT 
        CASE 
            WHEN income < 20000 THEN 'Low Salary'
            WHEN income BETWEEN 20000 AND 50000 THEN 'Average Salary'
            WHEN income > 50000 THEN 'High Salary'
        END AS category
    FROM Accounts
)
SELECT 
    a.category,
    COUNT(c.category) AS accounts_count
FROM all_categories a
LEFT JOIN category_count c
ON c.category = a.category
GROUP BY a.category;
```
