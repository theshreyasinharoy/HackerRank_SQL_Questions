# Weather Observation Station 9

#### Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

#### Input Format

#### The STATION table is described as follows:

![Station](https://github.com/user-attachments/assets/19b53825-9b07-455a-85e6-2f7617cc948b)

#### where LAT_N is the northern latitude and LONG_W is the western longitude.

---
#### Solution:-
```
SELECT
      DISTINCT city
FROM
      STATION
WHERE 
      LEFT(city,1) NOT IN ('a', 'e', 'i', 'o', 'u');
```
#### The ```LEFT()``` function in MySQL is used to extract a certain portion from the left side of a string. 

#### Here the first character is extracted using LEFT() and it is checked whether it is a vowel or not using ```NOT IN``` operator.

#### ```DISTINCT``` keyword in the ```SELECT``` clause is used to remove the duplicate city names.
