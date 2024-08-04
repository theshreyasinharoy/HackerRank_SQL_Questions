# Revising the Select Query 1

#### Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.

#### The CITY table is described as follows:

![City](https://github.com/user-attachments/assets/88817924-1d96-49e0-993e-ba1899d619db)

##### Solution:-
```
SELECT 
       *
FROM
       CITY
WHERE 
       COUNTRYCODE = "USA" AND
       POPULATION > 100000;
```
---

#### Here in the ```WHERE``` clause two conditions are applied using the ```AND``` logic to check the country code & population count.
