# Structured Query Language \(SQL\)

### Making Tables

```mysql
CREATE TABLE student (
    name VARCHAR(30),
    email VARCHAR(50)
);
```

### Inserting Data

```mysql
INSERT INTO student (name, email) VALUES
    ('Harry', 'harrisonturton@gmail.com'),
    ('John', 'john@bigpond.com.au');
```

Update single row:

```mysql
UPDATE student SET email='harryturton@gmail.com' WHERE name='Harry';
```

### Select Statements

```mysql
SELECT <attributes> FROM <one or more relations> WHERE <conditions>;
```

```mysql
SELECT * FROM students;
SELECT name, id FROM students WHERE id='1234' OR name='harry'
```

### Join Statements

```mysql
JOIN / LEFT JOIN / INNER JOIN / RIGHT JOIN /  OUTER JOIN
```

* **Inner Join **selects all_ \_records from A _and B where the join condition is met
* **Left Join **selects all records from A, along with records from B where the join condition is met
* **Right Join** selects all records from B, along with records from A where the join condition is met
* **Full Join **selects all records from A and B regardless of whether the condition is met

#### Inner Join

```mysql
customers = { customer_id, first_name, email, address }
orders    = { order_id, order_date, amount, customer_id }
```

```mysql
SELECT order_date, order_amount
FROM customers JOIN orders
    ON customers.customer_id = orders.customer_id
WHERE customer_id=3
```



