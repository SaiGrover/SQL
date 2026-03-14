# SQL Practice - First Names Starting and Ending with 's'

## Problem
https://www.sql-practice.com/

Show `patient_id` and `first_name` from the patients table where the `first_name`
starts and ends with **'s'** and is **at least 6 characters long**.

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
SELECT
  patient_id,
  first_name
FROM patients
WHERE first_name LIKE 's%s'
  AND LENGTH(first_name) >= 6;
```
