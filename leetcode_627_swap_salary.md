# LeetCode 627 - Swap Salary

## Problem
https://leetcode.com/problems/swap-salary/

## SQL Solution

```sql
UPDATE salary
SET sex =
CASE sex
    WHEN 'm' THEN 'f'
    ELSE 'm'
END;
```
