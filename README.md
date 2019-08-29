# PythonCheatSheet
A collection of python programming cheat sheet and tips

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


# Scikit Learn
## Pipeline
### fit, fit_transform
* Difference between fit() and fit_transform() *

https://datascience.stackexchange.com/questions/12321/difference-between-fit-and-fit-transform-in-scikit-learn-models


* A deep dive into sklearn pipelines *

https://www.kaggle.com/baghern/a-deep-dive-into-sklearn-pipelines


# Data Structure
### Tuple list to Dict
```
>>> my_list = [('a', 1), ('b', 2)]
>>> dict(my_list)
{'a': 1, 'b': 2}
```
