# SQL Practice - Repeated Diagnoses for a Patient

## Problem
https://www.sql-practice.com/

Show `patient_id` and `diagnosis` from the `admissions` table where the **same diagnosis occurs more than once for the same patient**.

## Schema

```sql
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
SELECT patient_id, diagnosis
FROM admissions
GROUP BY patient_id, diagnosis
HAVING COUNT(diagnosis) > 1;
```
