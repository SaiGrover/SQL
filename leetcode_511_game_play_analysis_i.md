# LeetCode 511 - Game Play Analysis I

## Problem
https://leetcode.com/problems/game-play-analysis-i/

## SQL Solution

```sql
SELECT player_id, MIN(event_date) AS first_login
FROM Activity
GROUP BY player_id;
