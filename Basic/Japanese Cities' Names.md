# Japanese Cities' Names

#### Query the names of all the Japanese cities in the CITY table. 

#### The COUNTRYCODE for Japan is JPN.

#### The CITY table is described as follows:

![City](https://github.com/user-attachments/assets/71a98731-2e41-4656-ae05-70f3a836f1f3)

#### Solution:-
```
SELECT
       NAME
FROM
       CITY
WHERE
       COUNTRYCODE = "JPN";
```
---
#### Querying the ```NAME``` of the Japanese cities in the ```SELECT``` clause while checking the ```COUNTRYCODE``` value in the ```WHERE``` clause.
