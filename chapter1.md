---
title       : Time Series with Pandas
description : Time Series with Pandas

--- type:NormalExercise lang:python xp:100 skills:2 key:3dc3440dc3
## Introduction to the dataset

In this chapter, we will be using a dataset that comes from a taxi company. 

Even plotting this messy data will be informative in many ways 

*** =instructions
- Investigate the dataset `taxi` using the Pandas head function
- We see that the `unix_timestamp` column isn't a proper datetime. Rather, it is a timestamp in unix form. Use `to_datetime` to convert this column to a datetime.
- How much is the median taxi fair for this driver?
- Let's plot the 

*** =hint
hint comes here

*** =pre_exercise_code
```{python}
import pandas as pd
taxi = pd.read_csv()

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


# Let's look at the plot visually. First we need to set the time as the index
taxi = taxi.set_index('unix_timestamp)

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
taxi = taxi.set_index('unix_timestamp)
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

