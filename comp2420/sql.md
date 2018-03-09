# Structured Query Language \(SQL\)

### Making Tables

```sql
CREATE TABLE student (
    name VARCHAR(30),
    email VARCHAR(50),
);
```

### Select Statements

```
SELECT <attributes> FROM <one or more relations> WHERE <conditions>;
```

```
SELECT * FROM students;
SELECT name, id FROM students WHERE id='1234' OR name='harry'
```

### Join Statements

```
JOIN / LEFT JOIN / INNER JOIN / RIGHT JOIN /  OUTER JOIN
```



