# LeetCode 1075 - Project Employees I

## Problem
https://leetcode.com/problems/project-employees-i/

## SQL Solution

```sql
SELECT p.project_id, AVG(e.experience_years) AS average_years
FROM Project p
JOIN Employee e 
ON p.employee_id = e.employee_id
GROUP BY p.project_id;
```
