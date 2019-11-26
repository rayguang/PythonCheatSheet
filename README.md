# PythonCheatSheet
A collection of python programming cheat sheet and tips

# Python tips
[Python anti-pattern](https://docs.quantifiedcode.com/python-anti-patterns/correctness/index.html): common problems with python coding

[Python gotcha](https://docs.python-guide.org/writing/gotchas/): useful advanced Python coding warnings/errors and fix


# Pandas
### Show all column names of pandas frame
```
pd.set_option('display.max_columns', None)
pd.set_option('display.max_rows', None)
```
### Convert Timestamp to epoch
```
df['creation_date'] = pd.to_datetime(df['creation_date']).values.astype(np.int64) // 1e9
```

# Data Structure
### Tuple list to Dict
```
>>> my_list = [('a', 1), ('b', 2)]
>>> dict(my_list)
{'a': 1, 'b': 2}
```

# Multiprocess
[Multiproc vs Multi Thread](https://stackoverflow.com/questions/3044580/multiprocessing-vs-threading-python)
