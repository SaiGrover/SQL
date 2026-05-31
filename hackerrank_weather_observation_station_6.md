# HackerRank - Weather Observation Station 6

## Problem

Query the list of `CITY` names starting with vowels (`a`, `e`, `i`, `o`, or `u`) from `STATION`.

Your result cannot contain duplicates.

## SQL Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE LEFT(CITY, 1) IN ('A', 'E', 'I', 'O', 'U');
```

## Explanation

- `LEFT(CITY, 1)` extracts the first character of each city name.
- `IN ('A', 'E', 'I', 'O', 'U')` filters cities that start with a vowel.
- `DISTINCT` removes duplicate city names from the result.

## Key Concepts

- String Functions (`LEFT`)
- Filtering (`WHERE`)
- Distinct Values (`DISTINCT`)
