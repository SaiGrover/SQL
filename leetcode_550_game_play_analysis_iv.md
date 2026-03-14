# LeetCode 550 - Game Play Analysis IV

## Problem
https://leetcode.com/problems/game-play-analysis-iv/

## SQL Solution

```sql
SELECT
  ROUND(
        COUNT(DISTINCT player_id) /
        (SELECT COUNT(DISTINCT player_id) FROM Activity),
        2
      ) AS fraction
FROM Activity
WHERE (player_id, DATE_SUB(event_date, INTERVAL 1 DAY)) IN (
        SELECT player_id, MIN(event_date)
        FROM Activity
        GROUP BY player_id
      );
