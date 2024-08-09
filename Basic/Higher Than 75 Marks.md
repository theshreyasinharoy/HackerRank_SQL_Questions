# Higher Than 75 Marks

#### Query the Name of any student in STUDENTS who scored higher than 75 Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.

#### Input Format

![Students](https://github.com/user-attachments/assets/7c2aaee6-b1ab-4253-b4f0-1686016fb958)

---

#### Solution:-
```
SELECT
         Name
FROM
         Students
WHERE
         Marks>75
ORDER BY
         RIGHT(Name,3), ID;
```
#### Names of those students are shown in the output whose marks satisfies the condition in the ```WHERE``` clause.

#### The ```Name``` values are ordered primarily by the last 3 characters of the names & then by ```ID``` values in ascending order using ```ORDER BY``` clause.
