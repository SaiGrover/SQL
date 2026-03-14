# LeetCode 596 - Classes With at Least 5 Students

## Problem
https://leetcode.com/problems/classes-with-at-least-5-students/

## SQL Solution

```sql
SELECT class
FROM Courses
GROUP BY class
HAVING COUNT(*) >= 5;
