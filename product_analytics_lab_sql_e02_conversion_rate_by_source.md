# Product Analytics Lab SQL E02 - Conversion Rate by Traffic Source

## Problem

https://product-analytics-lab.vercel.app/#/sql-lab/sql-e02

## SQL Solution

```sql
SELECT
    source,
    COUNT(*) AS total_sessions,
    SUM(CASE 
            WHEN converted THEN 1 
            ELSE 0 
        END) AS conversions,
    ROUND(
        100.0 * SUM(CASE 
                        WHEN converted THEN 1 
                        ELSE 0 
                    END) / COUNT(*),
        1
    ) AS conversion_pct
FROM sessions
GROUP BY source
ORDER BY conversion_pct DESC;
```
