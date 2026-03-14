# LeetCode 620 - Not Boring Movies

## Problem
https://leetcode.com/problems/not-boring-movies/

## SQL Solution

```sql
SELECT *
FROM Cinema
WHERE id % 2 != 0
  AND description != 'boring'
ORDER BY rating DESC;
```
