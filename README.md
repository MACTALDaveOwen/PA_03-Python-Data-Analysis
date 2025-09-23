# PA_03 Python Data Analysis

### Problem 01. Load CSV & Display Rows.

This program loads a .csv file into a pandas DataFrame named cars, and then displays the first five and last five rows of the dataset.
#### Functions utilized in Problem 01
```
pd.read_csv("file.csv")   - loads the CSV file into a DataFrame
head()                    - displays the first five rows of the DataFrame
tail()                    - displays the last five rows of the DataFrame
```
#### Code Overview

#### 1. Initialization

This codeblock imports panda to this program so that it can handle data from a .csv file. This then also reads the data stored in "cars.csv." 
~~~
import pandas as pd

#allows the program to read csv file
cars = pd.read_csv("cars.csv")
~~~
#### 2. Heads & Tails

This codeblock utilizes the .head and .tail built-in function in panda library. The '.head' prints the first five rows in the .csv file while '.tail' prints the last five rows of the file.
~~~
# prints the first five rows in the .csv file
print ("First Five Rows\n:")
print (cars.head())

# prints the last five rows in the .csv file
print ("\nLast Five Rows\n:")
print (cars.tail())
~~~

***

### Problem 02. Subsetting, Slicing, & Indexing with Dataframes.

This program extracts specific information from the cars dataset using pandas operations such as .iloc, .loc, and conditional filtering.

#### Functions utilized in Problem 02
```
iloc[rows, cols]       - used for integer-based indexing (row and column positions)
::2                    - slice notation that selects every second column (odd-numbered columns)
DataFrame[condition]   - filters rows based on a condition
loc[condition, cols]   - selects specific columns from rows that meet the condition
.values[0]             - extracts the first matching value from a Series
```

#### Code Overview

#### 1. Initialization

This codeblock imports panda to this program so that it can handle data from a .csv file. This then also reads the data stored in "cars.csv." 
~~~
import pandas as pd

cars = pd.read_csv("cars.csv")
~~~

#### 2. First Five Odd-Numbered Columns

This codeblock prints the first five odd-numbered columns of the data using the iloc[] function.
~~~
# displays the first five rows with odd-numbered columns
print ("A. First Five Rows with Odd-Numbered Columns:\n")
print (cars.iloc[0:5, ::2])
~~~

#### 3. Rows: Model, Mazda RX4

This codeblock prints the row the row that has 'Mazda RX4' as its model.
~~~
# displays the row that has the Model = Mazda RX4
print ("\nB. Rows that Contains the 'Mazda RX4': \n")
print (cars[cars["Model"] == "Mazda RX4"])
~~~

#### 4. Cylinder Count

This codeblock finds the row that has Camaro Z28 as its model and display its cylinder count.
~~~
# prints the number of cylinders in Camaro Z28
print ("\nC. Cylinders for Camaro Z28:")
print (cars.loc[cars["Model"] == "Camaro Z28", "cyl"].values[0])
~~~

#### 5. Cylinder & Gear Type

This codeblock finds the row of particular car models and display its cylinder and gear type
~~~
# prints the number of cylinders and gear type of various car models
print ("\nD. Cylinders & Gear Type for Mazda RX4 Wag, Ford Pantera L, & Honda Civic:\n")
print (cars.loc[
       (cars["Model"] == "Mazda RX4 Wag") |
       (cars["Model"] == "Ford Pantera L") |
       (cars["Model"] == "Honda Civic"),
       ["Model", "cyl", "gear"]])
~~~

Verson 02
