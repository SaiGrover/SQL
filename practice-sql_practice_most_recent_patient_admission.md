# SQL Practice - Most Recent Admission per Patient

## Problem
https://www.sql-practice.com/

Display every patient that has **at least one admission** and show their **most recent admission date** along with the **patient's full name** and the **doctor's full name**.

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

CREATE TABLE doctors (
    doctor_id INT,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    specialty VARCHAR(100)
);
```

## SQL Solution

```sql
SELECT
    CONCAT(p.first_name, ' ', p.last_name) AS patient_name,
    a.admission_date AS most_recent_admission,
    CONCAT(d.first_name, ' ', d.last_name) AS doctor_name
FROM admissions a
JOIN patients p 
    ON p.patient_id = a.patient_id
JOIN doctors d 
    ON a.attending_doctor_id = d.doctor_id
WHERE a.admission_date = (
    SELECT MAX(a2.admission_date)
    FROM admissions a2
    WHERE a2.patient_id = a.patient_id
);
```
