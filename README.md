# PA_03 Python Data Analysis

#### Problem 01. Load CSV & Display Rows.

This program loads a .csv file into a pandas DataFrame named cars, and then displays the first five and last five rows of the dataset.

```
pd.read_csv("file.csv")   - loads the CSV file into a DataFrame
head()                    - displays the first five rows of the DataFrame
tail()                    - displays the last five rows of the DataFrame
```

#### Problem 02. Subsetting, Slicing, & Indexing with Dataframes.

This program extracts specific information from the cars dataset using pandas operations such as .iloc, .loc, and conditional filtering.

```
iloc[rows, cols]       - used for integer-based indexing (row and column positions)
::2                    - slice notation that selects every second column (odd-numbered columns)
DataFrame[condition]   - filters rows based on a condition
loc[condition, cols]   - selects specific columns from rows that meet the condition
.values[0]             - extracts the first matching value from a Series
```
