# SQL Practice - Order Names by Length and Alphabetically

## Problem
https://www.sql-practice.com/

Display every patient's `first_name`.  
Order the list by the **length of each name** and then **alphabetically**.

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
SELECT first_name
FROM patients
ORDER BY LENGTH(first_name) ASC, first_name ASC;
```
