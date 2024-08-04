# Japanese Cities' Attributes

#### Query all attributes of every Japanese city in the CITY table. The COUNTRYCODE for Japan is JPN.

#### The CITY table is described as follows:

![City](https://github.com/user-attachments/assets/a7a4209d-dc4e-4188-8155-9573fd17d7af)

#### Solution:-
```
SELECT
       *
FROM
       CITY
WHERE
       COUNTRYCODE = "JPN";
```
---
#### Here in the ```WHERE``` clause a condition is applied to check the ```COUNTRYCODE``` value.
