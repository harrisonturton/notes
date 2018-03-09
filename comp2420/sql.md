# Structured Query Language \(SQL\)

### Making Tables

```mysql
CREATE TABLE student (
    name VARCHAR(30),
    email VARCHAR(50),
);
```

### Inserting Data

```
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

```
SELECT * FROM students;
SELECT name, id FROM students WHERE id='1234' OR name='harry'
```

### Join Statements

```mysql
JOIN / LEFT JOIN / INNER JOIN / RIGHT JOIN /  OUTER JOIN
```



