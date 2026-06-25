# Product Analytics Lab SQL E47 - Churned Subscriptions

## Problem

https://product-analytics-lab.vercel.app/#/sql-lab/sql-e47

## SQL Solution

```sql
SELECT 
    sub_id,
    account_id,
    plan_id,
    started_at,
    ended_at,
    mrr
FROM subscriptions
WHERE status = 'churned'
ORDER BY ended_at;
```
