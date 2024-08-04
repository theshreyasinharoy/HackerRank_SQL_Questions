# Revising the Select Query II

#### Query the NAME field for all American cities in the CITY table with populations larger than 120000. 

##### The CountryCode for America is USA.

#### The CITY table is described as follows:

![City](https://github.com/user-attachments/assets/ae0ca418-e197-4d75-84c6-041c8b1c5478)

#### Solution:-
```
SELECT
              NAME
FROM
              CITY
WHERE
              COUNTRYCODE = "USA" AND
              POPULATION > 120000;
```
---

#### Here quering only the ```NAME``` column in the ```SELECT``` clause while in the ```WHERE``` clause two conditions are applied using the ```AND``` logic to check the country code & population count.
