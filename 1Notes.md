# SQL
[Video Link](https://www.youtube.com/watch?v=7S_tz1z_5bA)

## DBMS
    1. RDBMS
        - Lang.: SQL
        - Eg.: MySql, SQL Server, Oracle
        - SQL is a language and MySQL is a software
    2. NOSql

## SQL
    - SQL is a language
    - It's not case sensitive
    - -- comment
    - USE -> to select DB to work with

### SELECT Command
```sql
    SELECT *
    SELECT DISTINCT first_name, last_name, (points*10)+100 AS discount
    FROM customer
    WHERE id = 1
    ORDER BY first_name
```
    - use '' if there is space in name
    - from, where, order by all are optional

### WHERE Command
```sql
    WHERE points (>,>=,<,<=,=,(!=,<>)) 3000
    WHERE NOT(points+40 > 3000 AND points < 4000 OR points > 5000)
    WHERE country NOT IN ('va','in','aus')
    WHERE points BETWEEN 1000 AND 2000 -> both are inclusive
    WHERE last_name LIKE 'b%' - '%ccc%' - '%e_q' - 's__a'
    WHERE last_name REGEXP 'field|mac|rob' - 'field$|mac|ro' - '^my|se'
```
    - AND has greater precedence
    - simplify NOT by changing individual operators
    - LIKE operator
        - %: any no. of character
        - _: single char
    - REGEXP operator
        - ^: beginning of string
        - $: end of string
        - |: logical OR
        - [gim]e
        - [a-h]b
