# SQL

## Basic Commands
### `SELECT` 

* &emsp; `*`

* &emsp; *col1*, ..., *coln*

&emsp; `FROM`

&emsp;&emsp; *table*

&emsp; `WHERE` *condition*

&emsp; `LIMIT` *n*

### `INSERT` `INTO`
&emsp;&emsp; *table* (*col1*, ..., *coln*)

&emsp; `VALUES` (*val1*, ..., *valn*)

### `UPDATE`
&emsp;&emsp; *table*

&emsp; `SET` *col1* = *val1*, ..., *coln* = *valn*

&emsp; `WHERE` *condition*

### `DELETE` `FROM`
&emsp;&emsp; *table*

&emsp; `WHERE` *condition*

## Operators

### Arithmetic
`+` `-` `*` `/` `%`
	
### Bitwise
`&` `|` `^`

### Logical
`ALL` `ANY` `EXISTS` `SOME` `AND` `OR` `XOR` `NOT` `IN` `BETWEEN` `LIKE '_%'`
		
### Comparison
`=` `>` `<` `>=` `<=` `<>`
	
## Grouping

### `GROUP` `BY`
&emsp;&emsp; *col1*, ..., *coln*

&emsp; `HAVING` *condition* (aggregates)

### `ORDER` `BY`
&emsp;&emsp; *col1* `ASC` | `DESC` , ..., *coln* `ASC` | `DESC`
	column with aggregates

## Functions
* `concat('Hello', ' ', 'World!',)` = 'Hello World!'
* `replace('abc','b','d')` = 'adc'
* `round(n, d)`
* `length(str)`
* `left('abc',1)` = 'a'
	
## Aggregates
`ALL` `ANY` `EXISTS` `MIN` `MAX` `COUNT` `SUM` `AVG` `DISTINCT`

`COALESCE(test_is_null_1, ..., test_is_null_n)`

`CASE` `WHEN` *condition* `THEN` *do* `ELSE` *do* `END`

## Database

### `CREATE` `DATABASE`
&emsp;&emsp; *db_name*

### `DROP` `DATABASE`
&emsp;&emsp; *db_name*

### `CREATE` `TABLE`
&emsp;&emsp; *table_name*

&emsp; `(`

&emsp;&emsp; *col1* `<datatype>` `<constraint>`,

&emsp;&emsp;&emsp; ...


&emsp;&emsp; *coln* `<datatype>` `<constraint>`,

&emsp;&emsp; `CONSTRAINT` *constraint_name* `<constraint>` (*val1*, ..., *valn*)

&emsp; `)`

### `ALTER` `TABLE`
&emsp;&emsp; *table_name*

* `ADD` *col* `<datatype>`
* `DROP` `COLUMN` *col*
* `RENAME` `COLUMN` *table_name* `TO` *new_table_name*
* `MODIFY` `COLUMN` *col* `<datatype>` `<constraint>`
* `ADD` `CONSTRAINT` *constraint_name* `<constraint>` (*col1*, ..., *coln*)
* `DROP` `CONSTRAINT` *constraint_name*

### `DROP` `TABLE`
&emsp;&emsp; *table_name*

## Data Types

### String
* `CHAR` (0 -> 255)
* `VARCHAR` (0 -> 65535)
* `BINARY(size)`
* `VARBINARY(size)`
* `BLOB` (0 -> 65535)
* `TEXT` (0 -> 65535) 
* `ENUM(val1, ..., valn)`

### Numeric
* `BOOLEAN`
* `BIT` (1->64)
* `INTEGER` (-2147483648 -> 2147483647)
* `FLOAT(size, d)`
* `DOUBLE(size, d)`
* `DECIMAL(size, d)`
	
### Datetime
* `DATE`
* `DATETIME(fsp)`
* `TIMESTAMP(fsp)`
* `TIME(fsp)`
* `YEAR`	

## Constraints
* `NOT` `NULL`
* `UNIQUE`
* `AUTO_INCREMENT`
* `PRIMARY` `KEY` (*col*)
* `FOREIGN` `KEY` (*col*) `REFERENCES` *other_table*(*col*)
* `CHECK`(*condition*)
* `DEFAULT`
	
## Joins

* (`INNER`) `JOIN` -> matches

* `LEFT` (`OUTER`) `JOIN` -> matches + left with no matches

* `RIGHT` (`OUTER`) `JOIN` -> matches + rigth with no matches

* `FULL` (`OUTER`) `JOIN` -> matches + left and rigth with no matches

* `UNION` -> distinct

* `UNION` `ALL` -> duplicates

## Stored Procedures
### `CREATE` `PROCEDURE`
&emsp;&emsp;&emsp; *procedure_name* 

&emsp;&emsp;&emsp; @*param_1* `<datatype>`,

&emsp;&emsp;&emsp;&emsp; ...

&emsp;&emsp;&emsp; @*param_n* `<datatype>`

&emsp;&emsp; `AS`

&emsp;&emsp; `BEGIN`

&emsp;&emsp;&emsp; ...


&emsp;&emsp; `END`

&emsp; `GO;`

### `EXEC`
&emsp;&emsp; *procedure_name* @*param_1* = *val1*, ..., @*param_n* = *valn*

### `DROP` `PROCEDURE`
&emsp;&emsp; *procedure_name*

## Views

### `CREATE`
&emsp;&emsp; *view_name* `AS` *query* 

### `SELECT`
&emsp;&emsp; ...

&emsp; `FROM`

&emsp;&emsp; *view_name*

### `REPLACE` `VIEW`
&emsp;&emsp; *view_name* `AS` *query* 

### `DROP` `VIEW`
&emsp;&emsp; *view_name*
	

# PYTHON

## Data Types

* `str`
* `int`, `float`, `complex`
* `list`, `tuple`, `range`
* `dict`
* `set`, `frozenset`
* `bool`
* `bytes`, `bytearray`, `memoryview`
* `NoneType`
	
## Operators

### Arithmetic
`+`, `-`, `*`, `/`, `//`, `**`, `%

### Assignment
`=`, `+=`, `...`,

`:=` walrus operator
		
### Comparison
`==`, `!=`, `<`, `>`, `<=`, `>=`
	
### Logical
`is` (`not`)

(`not`) `in`
		
`and`, `or`, `not`
		
### Bitwise
`&`, `|`, `^`, `~`, `<<`, `>>`


## String Methods

* `count()`
* `startswith()`
* `endswith()`
* `join()`
* `index()`
* `find()`
* `rfind()`
* `replace()`
* `strip()`
* `rstrip()`
* `lstrip()`
* `split()`
* `lower()`
* `upper()`
* `casefold()`
* `ljust()`
* `rjust()`

## Data Structures
	
### List
		
* Constructors
    * `[x**2 for x in range(10)]`
	
* Methods
    * `append()`
    * `extend()`
    * `insert()`
    * `remove()`
    * `pop()`
    * `clear()`
    * `index()`
    * `count()`
    * `reverse()`
    * `copy()`
    * `sort()`
	* `del a[n:m]`
			
### Tuple
Immutable list
`x, y, z = (1,1,1)`
		
* Methods
    * `count()`
    * `index()`
		
### Set
`a` - `b`

`a` | `b`

`a` & `b`

`a` ^ `b`

`a` < `b`

`a` > `b`
		
* Constructors
	* `set()`
	* `{1,2,3}`
	* `set('abba') = {'a', 'b'}`
	* `{x for x in {1,2,3} if x != 1}`
			
* Methods
    * `add()`
    * `clear()`
    * `copy()`
    * `difference()`
    * `discard()`
    * `intersection()`
    * `isdisjoint()`
    * `issubset()`
    * `issuperset()`
    * `pop()`
    * `remove()`
    * `symmetric_difference()`
    * `union()`
    * `update()`
		
 ### Dictionary
`in` (keys)
		
* Constructors
    * `{key: value}`
    * `dict((key, value), (key, value))`
    * `dict(key=value, key=value)`
    * `{x : x**2 for x in range(10)}`
			
* Methods
    * `clear()`
    * `copy()`
    * `get()`
    * `items()` [(key,value),...]
    * `keys()`
    * `values()`
    * `pop()`
    * `popitem()`
    * `setdefault()`
    * `update()`
    * `del` `d[key]`
    * `list(d)`, `sorted(d)` return a list of the keys
		
### Range
`range(i,f,s)`

`reversed()`
			
### collections.deque
* Constructors
    * `deque([a,b,c])`

* Methods
    * `append()`
    * `popleft()`
			
### Others
* Map
	* `map(func, iter, iter, ...)`
			
* Zip
	* `zip(iter, iter, iter, ...)`
			
* Enumerate
	* `list(enumerate(['a', 'b'], 5)) == [(5,'a'),(6,'b')]` 

* Enum

        from enum import Enum

            class A (Enum):

                a = val1

                b = val2

## Control Flow
	
### If
    if:

        do_smth

    elif:

        do_smth

    else:

        do_smth
	
### For
    for x in list:

        do_smth

    else:

        do_smth
    
    -> break/continue
		
### While
    while cond:

        do_smth

    else:

        do_smth
    
    -> break/continue
		
### Match
    match var:

        case c1:

            do_smth

        case cj | ck:

            do_smth

        case cn:

            do_smth

        case _:		

            do_smth
	
	
## Functions

`def` *func*(*arg1*, *arg2* = *<default_value>*, \**args*, \*\**kwargs*)
	
`def` *func*(*pos_arg*, `/`, *pos_or_kw_arg*, `*`, *kw_arg*)
	
There cannot be a positional argument after a keyword argument and the same for parameters that have a default value.
	
`def` *func*(*s*:*str* = "Hello") `->` *str*:

&emsp;&emsp; `return` s + "World!"
	
`lambda` *a*, *b*: a + b

## Input/Output

`f'Hola {var}'`

`'{:-1}{:2.2%}'.format(var, var)`

## Regex
`import re`

* Static
	* `compile()`
	* `split()`
* Methods
	* `search()`
	* `findall()`
	* `finditer()`
	* `match()`
        * `groups()`
	* `sub()`
	* `split()`
	

## Error-Handling

## Object-Oriented Programming

    class ChildClass(ParentClass, ...):

        def __init__(self, ...):
            self.var1 = ...
            self.__private_var1 = ...

        def method(self, ...):
            do_smth

        def __private_method(self, ...):
            do_smth

_
 
    class ChildClass(ParentClass, ...):

-

    from dataclasses import dataclass

    @dataclass
    class Employee:
        name: str
        dept: str
        salary: int


         

## Modules


## Virtual Environment

    python3 -m venv <project_venv>
    source project_venv/bin/activate
    deactivate
	
## PIP

    python -m pip install --user <package>
    python -m pip install --update <package>



# NUMPY

## Data Types

| TYPE | CODE |
| - | - |
| (`u`) `int8`, `16`, `32`, `64`  | `i1`, `u1`, ..., `i8`, `u8` |
| `float16`, `32`, `64`, `128` | `f2`, `f4`, `f8`, `f16` |
| `complex64`, `128`, `256` | `c8`, `c16`, `c32` |
| `bool` | `?` |
| `object` | `O` |
| `string_` | `S` |
| `unicode_` | `U` |


## numpy.array

### Constructors

* `array(arr[, dtype='<datatype>'])`
* `arange(k)`
* `zeros((n,m,...))`
* `ones((n,m,...))`
* `identity(n)`
* `diag(arr)`
* `block(np_arr,...)`
* `empty((n,m,...))`
* `full((n,m,...))`
* `where(bool_arr, arr, arr2)`

### Attributes
* `shape`
* `dtype`
* `ndim`
* `T`

### Shortcuts
* `arr` * `int`
* `arr` + `arr`
* `arr` - `arr`
* `arr` * `arr`: entry by entry
* `1` / `arr`
* `arr` ** `n`
* `arr` @ `arr2`: matrix multiplication
* `arr` <, >, ==, != `arr2`
* ~`bool_arr`
* `bool_arr` | `bool_arr2`
* `bool_arr` & `bool_arr2`

### Slicing/Access
* `arr[n:m]`
* `arr[n:m] = val`
* `arr[n:m] = array`
* `arr[n, m, ...]` is equivalent to `arr[n][m]...`
* `arr[[n, ...]]`
* `arr[[n, ...],[l, ...], ...]`
* `arr[:, [n, ...]]`
* `arr[n_1:m_1, n_2:m_2, ...]`
* `arr[bool_arr]`

### Methods
* `copy()`
* `astype(np.dtype)`
* `reshape((n_1, ..., n_m))`
* `transpose()`
* `swapaxes(n, m)`
* `sort()`


## Static

### Array Unary
* `abs()`
* `sqrt()`
* `square()`
* `exp()`
* `log()`
* `sign()`
* `ceil()`
* `floor()`
* `isnan()`
* `isfinite()`
* `isinf()`
* `cos()`, `arccos()`, `cosh()`, `arccosh()`, `...`
* `modf()`

The following unary functions do the operation over an axis, or the whole array:
* `sum()`, `cumsum()`
* `prod()`, `cumprod()`
* `min()`, `max()`
* `mean()`
* `std()`, `var()`
* `argmax()`, `argmin()`
* `any()`, `all()`
* `sort()`
* `unique()`

### Array Binary
* `add()`
* `subtract()`
* `multiply()`
* `divide()`, `floor_divide()`
* `power()`
* `maximum()`
* `minimum()`
* `mod()`
* `greater()`, `greater_equal()`
* `less()`, `less_equal()`
* `equal()`, `not_equal()`
* `logical_and`, `logical_or()`, `logical_xor()`
* `meshgrid()`: cartesian product
* `intersect1d()`
* `union1d()`
* `isin()`
* `setdiff1d()`
* `setxor1d()`
* `dot()`: matrix multiplication

### File
* `save("filename.npy", array)`
* `savez("filename.npz", a=arr, b=arr2, ...)`
* `savez_compressed("filename.npz", a=arr, b=arr2, ...)`
* `load("filename.npy")`


## numpy.random
`numpy.random.default_rng(seed=n)`
* `permutation(n)`, `permutation(arr)`
* `shuffle()`
* `uniform()`
* `integers()`
* `standard_normal(n)`, `standard_normal(size)`
* `binomial()`
* `normal()`
* `beta()`
* `chisquare()`
* `gamma()`


## numpy.linalg
* `diag()`
* `dot()`
* `trace()`
* `det()`
* `eig()`
* `inv()`
* `pinv()`
* `qr()`
* `svd()`
* `solve()`
* `lstsq()`



# PANDAS


## Static
* `na`
* `nan`
* `isna()`
* `isnan()`
* `value_counts()`


## pandas.Series

### Constructors
* `Series(arr[, index])`
* `Series(dict[, index])`

### Attributes
* `name`
* `dtype`
* `array`
* `index`
* `loc`
* `iloc`

### Shortcuts
* `ser` * `int`
* `ser` + `ser`
* `ser` - `ser`
* `ser` * `ser`
* `1` / `ser`
* `ser` ** `n`
* `ser` <, >, ==, != `ser2`
* ~`bool_ser`
* `bool_ser` | `bool_ser2`
* `bool_ser` & `bool_ser2`

### Slicing/Access
* `ser[bool_arr]`
* `ser.loc[["id1", ...]]`
* `ser.loc["id1":"id2"]` (inclusive)
* `ser.iloc[[n, m, ...]]`
* `ser.iloc[n:m]` (exclusive)

### Methods
* `get()`
* `to_dict()`
* `isna()`
* `notna()`
* `isin()`
* `reindex(indices_list[, method=])`
    * `method`: `'ffill'`, `'bfill'`
* `drop("id1")`
* `map(function)`
* `replace()`
    * `([from_val1, ...],[to_val1, ...])`
    * `({from_val: to_val, ... })`
* `sort_index([ascending])`
* `sort_values([ascending=, na_position=])`
    * `na_position`: `'first'`, `'last'`
* `unique()`
* `value_counts()`
* `sample(n=,[replace=])`

#### Arithmetic
numpy behaves well with pandas.Series

#### Descriptive/Statistics
* The same of data frames
* `argmin`, `argmax`
* `corr(ser2)`
* `cov(ser2)`

### String methods
The following methods are accessed by `ser.str.`*`method()`*
* `cat()`
* `contains()`
* `count()`
* `extract()`
* `endswith()`
* `startswith()`
* `findall()`
* `get()`
* `isalnum()`
* `isalpha()`
* `isdecimal()`
* `isdigit()`
* `islower()`
* `isupper()`
* `isnumeric()`
* `join()`
* `len()`
* `lower()`
* `upper()`
* `match()`
* `pad()`
* `center()`
* `repeat()`
* `replace()`
* `slice()`
* `split()`
* `strip()`
* `rstrip()`
* `lstrip()`


## pandas.DataFrame

### Constructors
* `DataFrame([[val, ...], ..., [val, ...]][, columns, index])`
* `DataFrame([{"col1":val, ...}, ..., {"col1": val, ...}])`
* `DataFrame(numpy_array)`
* `DataFrame({"col1": [val1, ...], ..., "coln": [val1, ...]}[, columns])`
* `DataFrame({"col1": {"id_1":val, ...}, ..., "coln": {"id_1": val, ...}}[, index])`
* `DataFrame({"col1": Series(), ...})`

### Attributes
* Columns are attributes
* `columns`
* `index`
* `loc`
* `iloc`
* `T`

### Slicing/Access
* `df["col"]`
* `df.<col>`
* `df[["col1", ...]]`
* `df.loc[:, ["col1", ...]]`
* `df[bool_array]`
* `df.loc["id1"]`
    * `df.loc["id1":"id2"]`
    * `df.loc[row, col]`
    * `df.loc[rows_arr, cols_arr]`
    * `df.loc[bool_series]`
    * `df.loc[bool_series, ["col1", ...]]`
* `df.iloc[i]`
    * `df.iloc[[n, m, ...]]`: rows n, m, ...
    * `df.iloc[n:m, l:k]`: rows from n to m, columns from l to k (exclusive)
* `df.at[row, col]`
* `df.iat[n_row, n_col]`

### Methods
* `head()`
* `tail()`
* `to_numpy()`
* `notna()`
* `isna()`
* `isin()`
* `reindex(index[, columns, axis, fill_value, method, limit, tolerance])`
    * `methods`: `'ffill'`, `'bfill'`
* `drop(index[, columns])`
* `apply(function[, axis])`
* `applymap(function)`
* `sort_index([axis, ascending])`
* `sort_values(['col1', ...])`
* `rank([axis, ascending, method])`
    * `methods`: `'average'`, `'min'`, `'max'`, `'first'`, `'dense'`
* `rename([index=dict, columns=dict])`
* `del df[col]`
* `any([axis=])`: boolean
* `all([axis=])`: boolean
* `nunique()`
* `value_counts()`: takes tuples as elements
* `df.apply(np.value_counts)`: takes the elements of each column
* `take(arr, [axis=])`
* `sample(n=,[replace=])`

#### Arithmetics
* `add(df[, fill_value, axis])`
* `sub()`
* `div()`
* `floordiv()`
* `mul()`
* `pow()`
* Each of these functions has a reversed function radd, rsub, ...
    * Another dataframe or series
    * `fill_value`
    * `axis` if a series is to be operated, it must match the axis (indexes or columns) [broadcasting]

#### Descriptive/Statistics
* `count()`
* `describe()`
* `min()`, `max()`
* `idxmin()`, `idxmax()`
* `quantile()`
* `sum()`
* `mean()`
* `median()`
* `mad()`: mean absolute deviation
* `prod()`
* `var()`
* `std()`: standard deviation
* `skew()`: skewness
* `kurt()`: kurtosis
* `cumsum()`
* `cummin()`, `cummax()`
* `cumprod()`
* `diff()`: first arithmetic difference
* `pct_change()`: percent change
* `corr()`
* `cov()`
* `corrwith()`
    * `axis`
    * `skipna`
    * `level`


## pandas.Index

### Attributes
* `name`
* `is_monotonic`
* `is_unique`

### Methods
* `append()`
* `difference()`
* `intersection()`
* `union()`
* `isin()`
* `delete()`
* `drop()`
* `insert()`
* `unique()`
* `get_indexer()`
* `map()`


## Data Loading

### import csv
* `csv.reader()`
* `csv.writer()`

### import json
* `loads()`: json string to dictionary
* `dumps()`: dictionary to json string

### import lxml, beautifulsoup4, html5lib
`from lxml import objectify`

`objectify.parse(file)`
* `getroot()`
	* `tag`, `pyval`

### read_csv()

* `path`
* `header`: number of the row which have the names of the columns 
* `names`: column names if header is None, or overrides them
* `index_col`: can be an array of indexes (hierarchical indexing)
* `sep`, `delimiter`
* `skiprows`
* `keep_default_na`
* `na_values`: array for all the table, dictionary to specify na values by column 
* `na_rep`
* `converters`: dictionary `{column: map}`
* `nrows`
* `date_parser`
* `iterator`
* `chunksize`
* `skip_footer`
* `index`
* `columns`
					
### read_excel()
`install openpyxl xlrd`

`pandas.ExcelFile(url)`
* `sheet_names`
* `parse(sheet_name="sheet1", index_col=n)`

`read_excel("", sheet_name="sheet1")`

`writer = pandas.ExcelWriter(url)`

`df.to_excel(writer, "sheet1")`

`writer.save()`

`df.to_excel(url)`
					
### read_sql()
`import sqlalchemy as sqla`

`sqla.create_engine(url)`

`pd.read_sql(query, db)`

### Others			
* `read_json()`: dataframes and series have a `to_json()` method
* `read_html()`: array of all the tables
* `read_xml`
* `read_stata()`
* `read_fwf()`
* `read_clipboard()`
* `read_hdf()`
* `read_feather()`
* `read_orc()`
* `read_parquet()`
* `read_pickle()`
* `read_sas()`
* `read_spss()`

### WEB API
`install requests`

`resp = requests.get(url)`

`resp.raise_for_status()`

`resp.json()`


## Data Cleaning

### Pandas

* `cut(data, bins[,right=, labels=, precision=])`
	* `codes`
    * `categories`
* `qcut(data, quartiles)`
* `get_dummies(df[, prefix=])` 
    * `str.get_dummies('<sep>')`

### Pandas Extension Data Types
* `BooleanDType`
* `CategoricalDtype`
* `DatatimeTZDtype`
* `Float32Dtype` (`64`)
* `Int8Dtype` (`16`, `32`, `64`)
* `UInt8Dtype` (`16`, `32`, `64`)

### Series
* `isna()`
* `notna()`
* `isnan()`
* `dropna()`
* `fillna([method])`

### DataFrames
* `isna()`
* `notna()`
* `isnan()`
* `dropna([axis=, how=,tresh=])`
	* `how`: `'all'`
	* `tresh`: number of na values not allowed
* `fillna(value, [method=, limit=, axis=])`
	* `value`: constant, dictionary `{'col': val}`
* `duplicated([keep=])`
* `drop_duplicates([subset=, keep=])`
	* `subset`: list of considered columns
	* `keep`: `"last"`
* mapping through columns (Series)
