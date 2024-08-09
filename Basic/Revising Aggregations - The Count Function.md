# Revising Aggregations - The Count Function

#### Query a count of the number of cities in CITY having a Population larger than 100,000.

#### Input Format

![City](https://github.com/user-attachments/assets/3dbab266-7dda-4f08-a382-640063a138f8)

---

#### Solution:-
```
SELECT
      COUNT(DISTINCT ID)
FROM
      CITY
WHERE
      POPULATION>100000;
```

