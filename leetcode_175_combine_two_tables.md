# LeetCode 175 - Combine Two Tables

## Problem
https://leetcode.com/problems/combine-two-tables/

## SQL Solution
```sql
SELECT p.FirstName, p.LastName, a.City, a.State
FROM Person p
LEFT JOIN Address a
ON p.PersonId = a.PersonId;
