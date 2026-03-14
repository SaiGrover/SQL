# SQL Practice - Format Patient Full Name

## Problem
https://www.sql-practice.com/

Display each patient's **full name in a single column** with the following format:

- `last_name` in **uppercase**
- `first_name` in **lowercase**
- Separate them with a **comma**

Example:
```
SMITH,jane
```

Order the list by **first_name in descending order**.

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
  CONCAT(UPPER(last_name), ',', LOWER(first_name)) AS new_name_format
FROM patients
ORDER BY first_name DESC;
```
