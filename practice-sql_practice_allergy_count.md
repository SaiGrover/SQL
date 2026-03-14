# SQL Practice - Count of Each Allergy

## Problem
https://www.sql-practice.com/

Show the number of patients for each **allergy** in the `patients` table.  
Exclude rows where the allergy is **NULL**.

Order the results by the **total count of each allergy in descending order**.

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
  allergies,
  COUNT(allergies) AS total_diagnosis
FROM patients
GROUP BY allergies
HAVING allergies IS NOT NULL
ORDER BY total_diagnosis DESC;
```
