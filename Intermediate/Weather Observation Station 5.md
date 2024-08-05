# Weather Observation Station 5

#### Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). 
#### If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.

#### The STATION table is described as follows:

![Station](https://github.com/user-attachments/assets/80e1391d-11c0-4efb-a6de-3df2befbec06)

#### Solution:-
```
WITH ranking AS (
SELECT 
       city, 
       LENGTH(city) AS length_of_city,
       RANK() OVER (ORDER BY   LENGTH(city) DESC, city) AS ranking_for_largest,
       RANK() OVER (ORDER BY   LENGTH(city) ASC, city) AS ranking_for_smallest
FROM 
       STATION
)
SELECT
       city,
       length_of_city
FROM
       ranking
WHERE
       ranking_for_smallest=1
             
UNION

SELECT
       city,
       length_of_city
FROM
       ranking
WHERE
       ranking_for_largest=1
```
---

#### Using a ```CTE```, ranks were assigned to the cities depending on the length of those city names.In the main query, two separate queries are written to extract the city 
##### names having the lowest and highest lengths.In the end, ```UNION``` operation is applied on those two queries.



