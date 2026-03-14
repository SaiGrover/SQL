# LeetCode 595 - Big Countries

## Problem
https://leetcode.com/problems/big-countries/

## SQL Solution

```sql
SELECT name, population, area
FROM World
WHERE area >= 3000000
   OR population >= 25000000;
