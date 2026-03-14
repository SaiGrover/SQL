# LeetCode 601 - Human Traffic of Stadium

## Problem
https://leetcode.com/problems/human-traffic-of-stadium/

## SQL Solution

```sql
WITH table1 AS (
    SELECT *
    FROM Stadium
    WHERE people >= 100
),
ranked AS (
    SELECT *,
           id - ROW_NUMBER() OVER (ORDER BY id) AS grp
    FROM table1
)

SELECT id, visit_date, people
FROM ranked
WHERE grp IN (
    SELECT grp
    FROM ranked
    GROUP BY grp
    HAVING COUNT(*) >= 3
)
ORDER BY visit_date;
