# Weather Observation Station 6

#### Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.

#### Input Format

#### The STATION table is described as follows:

![Station](https://github.com/user-attachments/assets/6bd7f0a4-a63d-46b0-9f74-781418fcd0e6)

#### where LAT_N is the northern latitude and LONG_W is the western longitude.

---

#### Solution:-
```
SELECT
      DISTINCT city
FROM
      STATION
WHERE 
      LEFT(city,1) IN ('a', 'e', 'i', 'o', 'u');
```
#### The ```LEFT()``` function in MySQL is used to extract a certain portion from the left side of a string. Here the first character is extracted using ```LEFT()``` and it is checked whether it is a vowel or not using ```IN``` operator. 
#### ```DISTINCT``` keyword in the select clause is used to remove the duplicate city names.


