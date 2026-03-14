# LeetCode 1934 - Confirmation Rate

## Problem
https://leetcode.com/problems/confirmation-rate/

## SQL Solution

```sql
WITH cte AS (
    SELECT
        s.user_id,
        SUM(CASE WHEN c.action = 'confirmed' THEN 1 ELSE 0 END) AS confirmed_count,
        COUNT(c.user_id) AS total_count
    FROM Signups s
    LEFT JOIN Confirmations c
        ON s.user_id = c.user_id
    GROUP BY s.user_id
)
SELECT
    user_id,
    ROUND(
        CASE WHEN total_count = 0 THEN 0
             ELSE confirmed_count / total_count
        END,
        2
    ) AS confirmation_rate
FROM cte
ORDER BY user_id;
```
