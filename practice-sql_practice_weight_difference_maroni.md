# SQL Practice - Weight Difference for Maroni

## Problem
https://www.sql-practice.com/

Show the **difference between the largest weight and the smallest weight** for patients with the last name **'Maroni'**.

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
SELECT MAX(weight) - MIN(weight) AS weight_delta
FROM patients
WHERE last_name = 'Maroni';
```
