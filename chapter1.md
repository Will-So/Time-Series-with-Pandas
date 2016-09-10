---
title       : Time Series with Pandas
description : Time Series with Pandas

--- type:NormalExercise lang:python xp:100 skills:2 key:3dc3440dc3
## A guided Tour Through the Dataset

In this chapter, we will be using a dataset that comes from a taxi company. First we will take a look at the first few trips in the table. After that we will make some changes to the dataframe so we can treat it as a time series. To finish off, we will examine the median fare charged  

Plotting the messy data will be informative in many ways. We'll be able to see the mininum and maximum of the data and eyeball if there are any trends in the data. For example, it could be that the taxi driver is doing ever longer or more expensive fares. Happily, Pandas makes it easy for us to do simple plots with its `.plot()` function.

There are a few important things to note when Using Pandas with Time Series. The first is that the time component must be the index. The second important detail is that Pandas must know this is a datetime. This is done with the `.to_datetime()` function.

*** =instructions
- Investigate the dataset `taxi` using the Pandas head function
- We see that the `unix_timestamp` column isn't a proper datetime. Rather, it is a timestamp in unix form. Use `to_datetime` to convert this column to a datetime.
- How much is the median taxi fair for this driver?
- Let's plot the time series and give it a nice title. Use the Pandas `.plot()` function for this. 

*** =hint
- Use `unit = 's'` in `to_datetime()` to tell Pandas that we are dealing with a unix type of date. 

*** =pre_exercise_code
```{python}
import pandas as pd
#taxi = pd.read_csv()

taxi = taxi.rename(columns={'unix timestamp': 'unix_timestamp'})
del taxi['id']
```

*** =sample_code
```{python}
import pandas as pd
%pylab inline

# Take a look at the dataset


# Change the unix_timestamp column to a proper datetime


# Take a look at the median fair amount


# Let's look at the plot visually. First we need to set the time as the index so Pandas knows
# How to plot the data
taxi = taxi.set_index('unix_timestamp')

```

*** =solution
```{python}
import pandas as pd
%pylab inline

# Take a look at the dataset
taxi.head()

# Change the unix_timestamp column to a proper datetime
taxi.unix_timestamp = pd.to_datetime(original_df.time, unit = 's')

# Take a look at the median fair amount
taxi.total_bill_usd.median()

# Let's look at the plot visually
taxi = taxi.set_index('unix_timestamp')
taxi.total_bill_usd.plot(title='Taxi Fairs Over Time (USD)');
```

*** =sct
```{python}
success_msg("Great work!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:b55d417ad6
## A way to deal with missing data

fillna(method='ffill'), resample() maybe linear interpolation

*** =instructions
- instruction 1
- instruction 2

*** =hint
hint comes here

*** =pre_exercise_code
```{python}
# pec
```

*** =sample_code
```{python}
# sample code
```

*** =solution
```{python}
# solution code
```

*** =sct
```{python}
success_msg("Great work!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:6144fd8b06
## Viewing the drivers' week

head(), median(), plot() Might have to set_index as well.

*** =instructions
- instruction 1
- instruction 2

*** =hint
hint comes here

*** =pre_exercise_code
```{python}
# pec
```

*** =sample_code
```{python}
# sample code
```

*** =solution
```{python}
# solution code
```

*** =sct
```{python}
success_msg("Great work!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:d348223843
## More Drivers

Groupby and then repeat the things from the previous section

*** =instructions
- instruction 1
- instruction 2

*** =hint
hint comes here

*** =pre_exercise_code
```{python}
# pec
```

*** =sample_code
```{python}
# sample code
```

*** =solution
```{python}
# solution code
```

*** =sct
```{python}
success_msg("Great work!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:b6a306f004
## A Simple Forecast

Use median of the last 5 weeks' rolling sum to do it (Forecast Vis -- give them the code)

*** =instructions
- instruction 1
- instruction 2

*** =hint
hint comes here

*** =pre_exercise_code
```{python}
# pec
```

*** =sample_code
```{python}
# sample code
```

*** =solution
```{python}
# solution code
```

*** =sct
```{python}
success_msg("Great work!")
```

