# LeetCode 602 - Friend Requests II: Who Has the Most Friends

## Problem
https://leetcode.com/problems/friend-requests-ii-who-has-the-most-friends/

## SQL Solution

```sql
WITH cte AS (
    SELECT requester_id AS id
    FROM RequestAccepted

    UNION ALL

    SELECT accepter_id AS id
    FROM RequestAccepted
)

SELECT id, COUNT(*) AS num
FROM cte
GROUP BY id
ORDER BY num DESC
LIMIT 1;
