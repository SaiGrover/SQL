# SQL Practice - Patients with Specific Allergies

## Problem
https://www.sql-practice.com/

Show `first_name`, `last_name`, and `allergies` from the patients table.  
Only include patients who are allergic to **Morphine** or **Penicillin**.

Order the result by:
1. `allergies`
2. `first_name`
3. `last_name`

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
  allergies
FROM patients
WHERE allergies = 'Morphine'
   OR allergies = 'Penicillin'
ORDER BY
  allergies,
  first_name,
  last_name;
```
