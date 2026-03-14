# SQL Practice - Unique Birth Years

## Problem
https://www.sql-practice.com/

Show unique birth years from patients and order them by ascending.

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
SELECT DISTINCT YEAR(birth_date) AS birth_year
FROM patients
ORDER BY birth_year;
```
