# SQL Practice - Count Male and Female Patients

## Problem
https://www.sql-practice.com/

Show the total amount of **male patients** and the total amount of **female patients** in the `patients` table.  
Display the two results in the **same row**.

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
  SUM(gender = 'M') AS male_count,
  SUM(gender = 'F') AS female_count
FROM patients;
```
