# LeetCode 608 - Tree Node

## Problem
https://leetcode.com/problems/tree-node/

## SQL Solution

```sql
SELECT id,
       CASE
           WHEN p_id IS NULL THEN 'Root'
           WHEN id IN (SELECT p_id FROM Tree) THEN 'Inner'
           ELSE 'Leaf'
       END AS type
FROM Tree;
