# SQL Practice - Number of Patients per City

## Problem
https://www.sql-practice.com/

Show the **city** and the **number of patients in each city** from the `patients` table.

Order the result by:
1. Number of patients in **descending order**
2. City name in **ascending order**

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
  city,
  COUNT(*) AS num_patients
FROM patients
GROUP BY city
ORDER BY COUNT(*) DESC, city ASC;
```
