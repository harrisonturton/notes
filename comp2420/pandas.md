# 

# Pandas

`pandas` is a library built on `numpy`. It provides easy ways to manipulate & analyze datasets.

### Dataframe

A `dataframe` is a 2D _labelled _structure. It's like a table - each column represents a different variable, and each row represents a different case. The first row is the _header row_, and contains labels for each column.

It is an way to give `pandas` knowledge of the semantic structure of your data, which influences how operations can be run.

![](/assets/Screen Shot 2018-03-19 at 11.04.46 am.png)

### Creating a DataFrame

```py
import pandas as pd

# A dictionary of lists, a dataset
studentData = {
    "id": [1,2,3,4],
    "name": ["Harry", "John", "Tess", "Alice"],
    "grade": [78.5, 58.3, 99.95, 83.4],
    "enrolled": [True, True, True, False] 
}

studentDataFrame = pd.DataFrame(studentData)
print(studentDataFrame)
#    enrolled  grade  id   name
# 0      True  78.50   1  Harry
# 1      True  58.30   2   John
# 2      True  99.95   3   Tess
# 3     False  83.40   4  Alice
```

### Indexing a DataFrame

By default, a `DataFrame` indexes by the order in which elements are given. We can index by an attribute:

```py
# Assume pandas & studentData (from above) is in our namespace

studentDataFrame.set_index("id", inplace=True)
```

The argument `inplace=True` means the method affects the given dataframe, rather than returning a new one.

### Filtering Columns

If a list of column names are provided as an index, only those columns are returned.

```py

print(studentDataFrame[["name", "grade"]])
#     name  grade
# 0  Harry  78.50
# 1   John  58.30
# 2   Tess  99.95
# 3  Alice  83.40
```

**Note:** The order of the columns is dependent upon the order in the index.

#### Selection

For this example, assume `dataframe` is a `DataFrame`.

| Operation | Syntax | Resulting Datatype |
| :--- | :--- | :--- |
| Selecting a column | dataframe\["column name"\] | Series |
| Selecting a row by label | dataframe.loc\[bool array, column\] | Series |
| Select a row by integer location | dataframe.iloc\[integer\] | Series |
| Slice rows | dataframe\[5:9\] | DataFrame |
| Slice rows by predicate | dataframe\[dataframe\["grade"\] &gt;= 55.0\] | DataFrame |



