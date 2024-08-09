# Weather Observation Station 11

#### Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.

#### Input Format

#### The STATION table is described as follows:

![Station](https://github.com/user-attachments/assets/5a178afe-bc35-4cf7-9b07-ffbe019717f4)

#### where LAT_N is the northern latitude and LONG_W is the western longitude.

---

#### Solution:-
```
SELECT
      DISTINCT city
FROM
      station
WHERE 
      LEFT(city,1) NOT IN ('a', 'e', 'i', 'o', 'u')  OR  
      RIGHT(city,1) NOT  IN  ('a', 'e', 'i', 'o', 'u');
```
#### The ```RIGHT()``` and ```LEFT()``` functions in MySQL are used to extract a certain portion from the right and left sides of a string respectively.

#### Here the first & last characters are extracted using these functions and it is checked whether they are vowels or not using ```NOT IN``` operator.

#### ```DISTINCT``` keyword in the ```SELECT``` clause is used to remove the duplicate city names.
