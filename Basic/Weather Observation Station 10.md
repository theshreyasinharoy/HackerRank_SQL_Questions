# Weather Observation Station 10

#### Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.

#### Input Format

#### The STATION table is described as follows:

![Station](https://github.com/user-attachments/assets/0b12fe93-76f6-4a53-8c89-e65c68cbe04f)

#### where LAT_N is the northern latitude and LONG_W is the western longitude.

---

#### Solution:-
```
SELECT
      DISTINCT city
FROM
      station
WHERE
      RIGHT(city,1)  NOT IN  ('a', 'e', 'i', 'o', 'u');
```
#### The ```RIGHT()``` function in MySQL is used to extract a certain portion from the right side of a string. 

#### Here the last character is extracted using ```RIGHT()``` and it is checked whether it is a vowel or not using ```IN``` operator.

#### ```DISTINCT``` keyword in the ```SELECT``` clause is used to remove the duplicate city names.

