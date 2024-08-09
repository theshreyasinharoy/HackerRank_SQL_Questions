# Employee Names

#### Write a query that prints a list of employee names (i.e.: the name attribute) from the Employee table in alphabetical order.

#### Input Format

#### The Employee table containing employee data for a company is described as follows:

![Employee](https://github.com/user-attachments/assets/6ba6384f-4584-4853-bb60-badcbc653212)

#### where employee_id is an employee's ID number, name is their name, months is the total number of months they've been working for the company, and salary is their monthly salary.
---
#### Solution:-
```
SELECT
         name
FROM
         Employee
ORDER BY
         name;
```
#### The ```name``` attribute values are retreived from the ```Employee``` table using the ```SELECT``` clause. 

#### The results are ordered in alphabetical order using ```ORDER BY``` clause.
