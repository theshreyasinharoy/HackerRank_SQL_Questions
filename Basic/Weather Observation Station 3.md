# Weather Observation Station 3

#### Query a list of CITY names from STATION for cities that have an even ID number. Print the results in any order, but exclude duplicates from the answer.

#### The STATION table is described as follows:

![Station](https://github.com/user-attachments/assets/7f79a285-d5bb-4939-85f6-ff0c959206ea)

---

#### Solution:-
```
SELECT
     DISTINCT city
FROM
     STATION
WHERE
     ID%2 = 0;
```
---

#### In the ```SELECT``` query, the ```CITY``` column is mentioned along with the ```DISTINCT``` keyword to remove duplicates. To check the ```ID``` value, a modulo operation on that value is performed in the ```WHERE``` clause.
