```sql
    SELECT city, LENGTH(city) AS "city Length"
    FROM station
    ORDER BY "city Length", city
    LIMIT 1;

    SELECT city, LENGTH(city) AS "city Length"
    FROM station
    ORDER BY "city Length" DESC, city
    LIMIT 1;
```

```sql
    SELECT DISTINCT city
    FROM station
    WHERE city REGEXP '^[AEIOUaeiou]'; -- regex for starting with vowels

    WHERE city REGEXP '^[^aeiouAEIOU].*' -- regex for not starting with vowels (^ acting as not in [])
```

```sql
SELECT SUM(c.population)
FROM city c
JOIN country co
ON c.countrycode = co.code AND co.continent = 'Asia';

same as

SELECT SUM(c.population)
FROM city c
JOIN country co
ON c.countrycode = co.code
WHERE co.continent = 'Asia';
```

SQL's aggregation functions like MIN are used to calculate a single value from a set of values, and they don't return the corresponding non-aggregated columns without a group or additional logic.