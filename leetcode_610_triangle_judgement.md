# LeetCode 610 - Triangle Judgement

## Problem
https://leetcode.com/problems/triangle-judgement/

## SQL Solution

```sql
SELECT *,
       IF(x + y > z AND y + z > x AND x + z > y, 'Yes', 'No') AS triangle
FROM Triangle;
