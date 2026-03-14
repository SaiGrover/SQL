# LeetCode 178 - Rank Scores

## Problem
https://leetcode.com/problems/rank-scores/

## SQL Solution

```sql
SELECT
    score,
    DENSE_RANK() OVER (ORDER BY score DESC) AS rank
FROM Scores
ORDER BY score DESC;
