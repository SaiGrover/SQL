# Product Analytics Lab SQL E44 - Premium Users by Device OS

## Problem

https://product-analytics-lab.vercel.app/#/sql-lab/sql-e44

## SQL Solution

```sql
SELECT 
    device_os,
    COUNT(*) AS total_users,
    SUM(is_premium) AS premium_users,
    ROUND(
        100 * SUM(is_premium) / COUNT(*),
        1
    ) AS premium_pct
FROM users
GROUP BY device_os;
```
