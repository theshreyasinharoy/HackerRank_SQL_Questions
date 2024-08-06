# The Report
#### You are given two tables: Students and Grades. Students contains three columns ID, Name and Marks.

![Students](https://github.com/user-attachments/assets/d63a6f16-31ab-4f13-bdc3-511e83ff05c9)

#### Grades contains the following data:

![Grades](https://github.com/user-attachments/assets/a838b6a8-fe97-4e8d-be11-f71326e78818)

#### Ketty gives Eve a task to generate a report containing three columns: Name, Grade and Mark. Ketty doesn't want the NAMES of those students who received a grade lower than 8. The report must be in descending order by grade -- i.e. higher grades are entered first. If there is more than one student with the same grade (8-10) assigned to them, order those particular students by their name alphabetically. Finally, if the grade is lower than 8, use "NULL" as their name and list them by their grades in descending order. If there is more than one student with the same grade (1-7) assigned to them, order those particular students by their marks in ascending order.

#### Write a query to help Eve.

---

#### Solution:-
```
WITH grading AS (
SELECT
     name,
     CASE
          WHEN marks>=0 AND marks<=9 THEN 1
          WHEN marks>=10 AND marks<=19 THEN 2
          WHEN marks>=20 AND marks<=29 THEN 3
          WHEN marks>=30 AND marks<=39 THEN 4
          WHEN marks>=40 AND marks<=49 THEN 5
          WHEN marks>=50 AND marks<=59 THEN 6
          WHEN marks>=60 AND marks<=69 THEN 7
          WHEN marks>=70 AND marks<=79 THEN 8
          WHEN marks>=80 AND marks<=89 THEN 9
          WHEN marks>=90 AND marks<=100 THEN 10
      END AS Grade,
      marks
FROM 
      Students
)
SELECT
         CASE
             WHEN Grade>= 8 THEN name
             ELSE null
         END AS Std_name,
         Grade,
         marks
FROM 
         grading
ORDER BY
         Grade DESC,
         Std_name,
         marks;
```
#### Using a CTE, the grades are applied to all the students according to the provided grading system. In the main query, a CASE statement is used to check the grade. According to the grade value, the name of the student or the null value is shown as output.


