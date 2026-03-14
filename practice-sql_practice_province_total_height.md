# SQL Practice - Provinces with Total Height ≥ 7000

## Problem
https://www.sql-practice.com/

Show the `province_id` and the **sum of heights of patients** in each province.  
Only include provinces where the **total height is greater than or equal to 7000**.

## Schema

```sql
CREATE TABLE patients (
    patient_id INT,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    gender VARCHAR(10),
    birth_date DATE,
    city VARCHAR(50),
    province_id VARCHAR(10),
    allergies VARCHAR(50),
    height INT,
    weight INT
);
```

## SQL Solution

```sql
SELECT province_id, SUM(height) AS sum_height
FROM patients
GROUP BY province_id
HAVING SUM(height) >= 7000;
```
