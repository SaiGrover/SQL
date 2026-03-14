# SQL Practice - Patients Without Admissions

## Problem
https://www.sql-practice.com/

Show `patient_id`, `first_name`, and `last_name` from the `patients` table for patients who **do not have any records in the admissions table**.

Their `patient_id` should **not exist in any `admissions.patient_id` rows**.

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
SELECT patient_id, first_name, last_name
FROM patients
WHERE patient_id NOT IN (
    SELECT patient_id
    FROM admissions
);
```
