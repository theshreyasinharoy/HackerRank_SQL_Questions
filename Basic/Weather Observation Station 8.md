# Weather Observation Station 8

#### Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.

#### Input Format

#### The STATION table is described as follows:

![Station](https://github.com/user-attachments/assets/7851da88-6824-4eb1-b45c-5f72b2d54f01)

#### where LAT_N is the northern latitude and LONG_W is the western longitude.

---

#### Solution:-
```
SELECT
      DISTINCT city
FROM
      station
WHERE 
      LEFT(city,1) IN ('a', 'e', 'i', 'o', 'u') AND  RIGHT(city,1)  IN  ('a', 'e', 'i', 'o', 'u');
```
#### The ```RIGHT()``` and ```LEFT()``` functions in MySQL are used to extract a certain portion from the right and left sides of a string respectively. 

#### Here the first & last characters are extracted using these functions and it is checked whether they are vowels or not using ```IN``` operator.

#### ```DISTINCT``` keyword in the ```SELECT``` clause is used to remove the duplicate city names.
