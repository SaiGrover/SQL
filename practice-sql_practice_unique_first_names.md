# SQL Practice - Unique First Names

## Problem
https://www.sql-practice.com/

Show unique first names from the patients table which only occur once in the list.

For example, if two or more people are named 'John' in the `first_name` column then don't include their name in the output list. If only 1 person is named 'Leo' then include them in the output.

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
GROUP BY first_name
HAVING COUNT(first_name) = 1
ORDER BY first_name ASC;
```
