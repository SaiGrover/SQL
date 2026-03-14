# LeetCode 619 - Biggest Single Number

## Problem
https://leetcode.com/problems/biggest-single-number/

## SQL Solution

```sql
SELECT MAX(num) AS num
FROM MyNumbers
WHERE num IN (
    SELECT num
    FROM MyNumbers
    GROUP BY num
    HAVING COUNT(*) = 1
);
