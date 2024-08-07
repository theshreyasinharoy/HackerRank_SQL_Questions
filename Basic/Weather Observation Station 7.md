# Weather Observation Station 7

#### Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.

#### Input Format

#### The STATION table is described as follows:

![Station](https://github.com/user-attachments/assets/99f39cf3-b766-413e-8754-ea7a7f3d06fe)

#### where LAT_N is the northern latitude and LONG_W is the western longitude.

---

#### Solution:-
```
SELECT
      DISTINCT city
FROM
      station
WHERE
      RIGHT(city,1)  IN  ('a', 'e', 'i', 'o', 'u');
```
#### The ```RIGHT()``` function in MySQL is used to extract a certain portion from the right side of a string. Here the last character is extracted using RIGHT() and it is checked whether it is a vowel or not using ```IN``` operator.
#### ```DISTINCT``` keyword in the ```SELECT``` clause is used to remove the duplicate city names.
