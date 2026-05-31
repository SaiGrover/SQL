# HackerRank - Weather Observation Station 5

## Problem

Query the two cities in `STATION` with the shortest and longest `CITY` names, along with their respective lengths.

If there is more than one shortest or longest city, choose the city that comes first alphabetically.

## SQL Solution

### Shortest City Name

```sql
SELECT CITY, LENGTH(CITY)
FROM STATION
ORDER BY LENGTH(CITY), CITY
LIMIT 1;
```

### Longest City Name

```sql
SELECT CITY, LENGTH(CITY)
FROM STATION
ORDER BY LENGTH(CITY) DESC, CITY
LIMIT 1;
```

## Explanation

- `LENGTH(CITY)` calculates the number of characters in each city name.
- For the shortest city, records are sorted by length in ascending order and then alphabetically.
- For the longest city, records are sorted by length in descending order and then alphabetically.
- `LIMIT 1` ensures that only the required city is returned.

## Key Concepts

- String Functions (`LENGTH`)
- Sorting (`ORDER BY`)
- Tie Breaking
- Limiting Results (`LIMIT`)
