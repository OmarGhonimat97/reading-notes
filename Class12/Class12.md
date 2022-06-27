## Pandas in 10

> Object creation & Viewing data


In this introduction to pandas, it shows how to create an object.
Then how to view the data created.

> Selection

While standard Python / NumPy expressions for selecting and setting are intuitive and come in handy for interactive work, for production code, it is recommended to use the optimized pandas data access methods, .at, .iat, .loc and .iloc.

- Getting
- Selection by label
- Selection by position
- Boolean indexing
- Setting


> Missing data

pandas primarily uses the value np.nan to represent missing data. It is by default not included in computations.

Reindexing allows you to change/add/delete the index on a specified axis.This returns a copy of the data.

> Operations

- Stats
- Apply
- Histogramming
- String Methods

>> Merge

- Concat
- Join

> Grouping


By “group by” we are referring to a process involving one or more of the following steps:
- Splitting the data into groups based on some criteria
- Applying a function to each group independently
- Combining the results into a data structure

> Reshaping

- Stack
- Pivot tables

> Time series

pandas has simple, powerful, and efficient functionality for performing resampling operations during frequency conversion (e.g., converting secondly data into 5-minutely data). This is extremely common in, but not limited to, financial applications.

> Categoricals

pandas can include categorical data in a DataFrame. 

> Plotting

> Getting data in/out

- CSV
- HDF5
- Excel

> Gotchas



