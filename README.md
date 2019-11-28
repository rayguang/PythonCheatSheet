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
#### Merge, Join vs Concat
[Stackoverflow comparison](https://stackoverflow.com/questions/40468069/merge-two-dataframes-by-index)

[Pandas Official Guide](https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html)

[Martin-thoma Blog on merge, join and concat](https://martin-thoma.com/pandas-merge-join-concatenate/)

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

[Parallel CPU Bound Tasks with Multiproc](https://eli.thegreenplace.net/2012/01/16/python-parallelizing-cpu-bound-tasks-with-multiprocessing/)
