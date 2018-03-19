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
| ERROR: no schema has been selected to create in LINE 1: create table ... | No 'public' schema. | CREATE SCHEMA public; See: https://stackoverflow.com/questions/14285854/cannot-create-a-new-table-after-drop-schema-public |



