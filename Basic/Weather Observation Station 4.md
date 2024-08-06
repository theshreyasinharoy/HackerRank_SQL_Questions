# Weather Observation Station 4

#### Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.

#### The STATION table is described as follows:

![Station](https://github.com/user-attachments/assets/52a6b262-22db-4362-a7b6-9506c8e350cf)

#### where LAT_N is the northern latitude and LONG_W is the western longitude.

---

#### Output:-
```
SELECT 
      COUNT(city) - COUNT(DISTINCT city) AS city_count
FROM 
      STATION;
```

#### Using ```COUNT``` function we are counting the number of all cities and while using ```DISTINCT``` keyword along with the city name, we are getting the count of distinct city names. Then subtracting the latter from the former is yielding the result.

