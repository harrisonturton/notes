# PSQL Cheatsheet

**Begin PSQL session**

```
$ psql
```

### Basic Commands

**Exiting**

```
\q
```

**Clear Screen**

```
(ctrl+l)
```

**Display Tables**

```
\dt
```

**Help on SQL commands**

```
\h
```

**Load commands from file**

```
\i <filepath>
```

### Past Errors

| Error Message | Cause | Solution |
| :--- | :--- | :--- |
| ERROR: no schema has been selected to create in LINE 1: create table ... | No 'public' schema. | CREATE SCHEMA public; See: [https://stackoverflow.com/questions/14285854/cannot-create-a-new-table-after-drop-schema-public](https://stackoverflow.com/questions/14285854/cannot-create-a-new-table-after-drop-schema-public) |

# Assignment

100 marks total.

1. 15 marks
2. 10 marks
3. 7.5 marks
4. 17.5 marks
5. 30 marks
6. 20 marks

**Order of marks: **Five, Six, Four, Three, One, Two

![](/assets/schema_tables_diagram.png)

#### Part One \(15 marks\)

Find the sections that had maximum enrollment in Spring 2009.

```sql
-- Find the no. of students enrolled per section
WITH enrollment AS (
 SELECT sec_id, COUNT(*) as num_enrolled
  FROM takes
  GROUP BY sec_id)
SELECT sec_id as max_enrolled
FROM enrollment
-- Find the section which has the max no. of enrollments
WHERE num_enrolled=(
 SELECT MAX(num_enrolled)
 FROM enrollment)
```



For all instructors, show their ID, name & number of sections they've taught. For instructors who haven't taught any sections, display 0 as the number of sections taught.

      1 WITH instructor_teaches AS (
      2     SELECT DISTINCT instructor.id, instructor.name, teaches.course_id, teaches.sec_id
      3     FROM instructor
      4     LEFT JOIN teaches
      5     ON instructor.id = teaches.id)
      6 SELECT name, COUNT(sec_id)`
      7 FROM instructor_teaches
      8 GROUP BY name;
      9
     10 SELECT name, COUNT(sec_id)
     11 FROM (
     12     SELECT DISTINCT i.id, i.name, t.course_id, t.sec_id
     13     FROM instructor as i
     14     LEFT JOIN teaches as t
     15     ON i.id = t.id) as instructor_teaches
     16 GROUP BY name;



Find all \(instructor, section\) where an instructor teaches sections in two different classrooms in a semester at the same timeslot.

Display a list of all students in the CS department, along with course sections they've taken in Spring 2009 \(if any\). All course sections from Spring 2009 must be displayed, even if no student from the CS dept. has taken it.

Find all departments where the total salary is greater than the average of the total salary at all departments.

Display the name of each instructor along with their department name, their salary, and the average salary of their department.

#### Part Two \(10 marks\)

We want to write a query that to "List the names of instructors & the titles of the courses they teach".

What is wrong with the output of this query? Explain your reasoning, and give a test dataset that can help use catch the error.

```rust
select name, title
from instructor natural join teaches natural join course;
```

#### Part Three \(7.5 marks\)

Consider the following schema:

* Suppliers
  * `sid INTEGER`
  * `sname STRING`
  * `address STRING`
* Parts
  * `pid INTEGER`
  * `pname STRING`
  * `color STRING`
* Catalog
  * `sid INTEGER`
  * `pid INTEGER`
  * `cost REAL`

Write relational algebra \(NOT SQL\) for the following queries:

1. Find the SID's of suppliers who supply a _red part _**or **are at _221 Packer Street._
2. Find the SID's of suppliers who supply some _red_ **or **\_green \_part.
3. Find the PID's of the parts supplied by Yosemite Sham \(a supplier\).

#### 

#### Part Four \(17.5 marks\)

Consider Q3, and state \(in plain English\) the output of these relation algebra queries:

...

Write the resulting SQL queries

#### Part Five \(30 marks\)

Draw an ER model for the data described below.

#### Part Six \(20 marks\)

Answer the following:

...

