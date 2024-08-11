# JOINS

### Joins Inner

```sql
    SELECT order_id, o.cust_id, p.product_id
    FROM order o
    JOIN product p
    ON o.cust_id = p.cust_id
```

### Joining across databases
```sql
    SELECT order_id, p.product_id
    FROM sql_inventory.order o
    JOIN product p
    ON o.cust_id = p.cust_id
```

### Self Join
```sql
    SELECT emp_id, m.first_name, m.emp_id
    FROM employee e
    JOIN employee m
    ON e.reports_to = m.emp_id
```

### Joining Multiple Tables
```sql
    SELECT emp_id, first_name
    FROM employee e
    JOIN product p
    ON e.emp_id = p.emp_id
    JOIN workstatus ws
    ON p.emp_id = ws.work_id
```
