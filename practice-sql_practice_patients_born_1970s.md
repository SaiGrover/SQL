# SQL Practice - Patients Born in the 1970s

## Problem
https://www.sql-practice.com/

Show all patient's `first_name`, `last_name`, and `birth_date` who were born in the **1970s decade**.  
Sort the list starting from the **earliest birth_date**.

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
  first_name,
  last_name,
  birth_date
FROM patients
WHERE birth_date BETWEEN '1970-01-01' AND '1979-12-31'
ORDER BY birth_date ASC;
```
