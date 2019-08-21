# PythonCheatSheet
A collection of python programming cheat sheet and tips

## Pandas
### Show all column names of pandas frame
```
pd.set_option('display.max_columns', None)
pd.set_option('display.max_rows', None)
```
### Convert Timestamp to epoch
```
df['creation_date'] = pd.to_datetime(df['creation_date']).values.astype(np.int64) // 1e9
```
