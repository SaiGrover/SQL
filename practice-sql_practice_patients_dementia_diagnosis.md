# SQL Practice - Patients Diagnosed with Dementia

## Problem
https://www.sql-practice.com/

Show `patient_id`, `first_name`, and `last_name` from the patients table whose diagnosis is **'Dementia'**.

The **primary diagnosis** is stored in the `admissions` table.

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

CREATE TABLE admissions (
    patient_id INT,
    admission_date DATE,
    discharge_date DATE,
    diagnosis VARCHAR(100),
    attending_doctor_id INT
);
```

## SQL Solution

```sql
SELECT
  p.patient_id,
  p.first_name,
  p.last_name
FROM patients p
JOIN admissions a
  ON p.patient_id = a.patient_id
WHERE a.diagnosis = 'Dementia';
```
