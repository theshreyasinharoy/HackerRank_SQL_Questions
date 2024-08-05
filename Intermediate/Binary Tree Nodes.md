# Binary Tree Nodes

#### You are given a table, BST, containing two columns: N and P, where N represents the value of a node in Binary Tree, and P is the parent of N.

#### Write a query to find the node type of Binary Tree ordered by the value of the node. Output one of the following for each node:

![BST](https://github.com/user-attachments/assets/f70a4bef-5c99-4c87-810e-2dc6d1afe725)

#### - Root: If node is root node.
#### - Leaf: If node is leaf node.
#### - Inner: If node is neither root nor leaf node.

#### Solution:-
```
SELECT
             N,
             CASE
                  WHEN P IS null THEN "Root"
                  WHEN N IN 
                  (SELECT 
                         DISTINCT P 
                   FROM 
                         BST) THEN "Inner"
                   ELSE "Leaf"
             END AS node_type
FROM
             BST
ORDER BY
             N;
```
---
#### Using a ```CASE``` statement, three scenarios are implemented. If a node does not have any parent value then it means it's the ```Root``` node. 
#### Otherwise, if that node value is present in the P column then it's an ```Inner``` node.This scenario is checked using a subquery.
#### If both these two conditions fail then that node is a ```Leaf``` node.
