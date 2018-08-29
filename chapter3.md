---
title: 'Data Manipulations with Dplyr'
description: ""
---

## Insert exercise title here

```yaml
type: VideoExercise 
xp: 50 
key: 3769fa8b9b   
```

`@projector_key`
dd4e6085bd7725c658ebc41bb0ea17f0
---

## Selecting variables

```yaml
type: NormalExercise 
xp: 100 
key: 6987bd7422   
```


We can subset the columns (variables) that matter by using `select()`.

As an example, take the following call, that selects the variables var1 and var2 from the data frame df.

`select(df, var1, var2)`

You can also select columns based on the index of the column (position of the column). For instance, for selecting columns: one, three and five; you can use:

`select(df, 1,3,5)`

In addition, you can use `:` to select a range of variables and `-` to exclude some variables. For instance:

`select(df, 1:4, -2)`

`select()` does not change the data frame it is called on; you have to explicitly assign the result of `select()` to a variable (or object) to store the result.


`@instructions`
Using the dataframe `data`, create an new variable called: `new.data` containing the range of columns from the first to the fifth column, excluding Horse Power (hp)

`@hint`


`@pre_exercise_code`

```{r}
#install.packages('dplyr')
library('dplyr')
data<-mtcars
```


`@sample_code`

```{r}
# Select first to fifth column excluding hp
#new.data<- ____

# See the output of your code
#head(____)
```


`@solution`

```{r}
new.data<- select(data,1:5,-hp)
```


`@sct`

```{r}

```


---

## Helper functions for variable selection

```yaml
type: NormalExercise 
xp: 100 
key: 6944788821   
```


`dplyr` comes with a set of helper functions that can help you select groups of variables inside a select() call. Some of the most important are:

- `starts_with("X"):` every name that starts with "X",
- `ends_with("X"):` every name that ends with "X",
- `contains("X"): `every name that contains "X",
- `matches("X"):` every name that matches "X", where "X" can be a regular expression,

Pay attention here: When you refer to columns directly inside select(), you don't use quotes. If you use the helper functions, you do use quotes.

For instance, to select from 'yourdata' only those columns containing the word "year" in their name, you can use:
`select(yourdata, contains("year"))`


`@instructions`
Create a new object called `variables` including only those columns from `data` starting with the letter 'b'.

`@hint`


`@pre_exercise_code`

```{r}
require(dplyr)
data<-mtcars
```


`@sample_code`

```{r}
# Subset columns starting with 'd' and store them in a new object called 'variables'.
```


`@solution`

```{r}

```


`@sct`

```{r}

```


---

## Mutating  (creating)

```yaml
type: NormalExercise 
xp: 100 
key: 5815ff4cda   
```


`mutate()` creates new columns which are added to a copy of the dataset.

Take this example that adds a new column, z, which is the element-wise sum of the columns x and y, to the data frame df:

`mutate(df, z = x + y)`

In the previous example, if there was a column already called `z`, R would replace the column values with the new calculation. Otherwise, a new column called `z` will be created with the calculation. 

You can also use mutate() to add multiple variables at once. Just place a comma between each variable that you define inside mutate().

In the following example, a new variable `x` is directly reused to create the new variable `y`:

`mutate(my_data, x = a + b, y = x + c)`


`@instructions`
Create a new object called kilometres. The new object must contain the `data` about cars plus an additional column estimating the kilometres per gallon (kpg) consumed by the vehicles.  

One mile per gallon `(mpg)` is equivalent to 1.609 kpg.

`@hint`
Multiply the column mpg by 1.609 (`mpg * 1.609`)

`@pre_exercise_code`

```{r}
data<-mtcars
```


`@sample_code`

```{r}
# Create a new aobject including an addictional column with the kilometres per gallog (kpg)
```


`@solution`

```{r}

```


`@sct`

```{r}

```


---

## Filtering records

```yaml
type: NormalExercise 
xp: 100 
key: 27077dd3ca   
```


`Filter()` can be used the subset records based on a given criteria. R comes with a set of logical operators that you can use inside filter():

- `x < y`, TRUE if `x` is less than `y`
- `x <= y`, TRUE if `x` is less than or equal to `y`
- `x == y`, TRUE if `x` equals `y`
- `x != y`, TRUE if `x` does not equal `y`
- `x >= y`, TRUE if `x` is greater than or equal to `y`
-` x > y`, TRUE if `x` is greater than `y`
- `x %in% c(a, b, c)`, TRUE if x is in the vector c(a, b, c)

The following example filters `df` such that only the observations for which a is positive, are kept:

`filter(df, a > 0)`


`@instructions`


`@hint`


`@pre_exercise_code`

```{r}
data<- mtcars
```


`@sample_code`

```{r}

```


`@solution`

```{r}

```


`@sct`

```{r}

```


---

## Insert exercise title here

```yaml
type: NormalExercise 
xp: 100 
key: a4256ea51e   
```


Combining tests using boolean operators
R also comes with a set of boolean operators that you can use to combine multiple logical tests into a single test. These include & (and), | (or), and ! (not). Instead of using the & operator, you can also pass several logical tests to filter(), separated by commas. The following two calls are completely equivalent:

filter(df, a > 0 & b > 0)
filter(df, a > 0, b > 0)
Next, is.na() will also come in handy. This example keeps the observations in df for which the variable x is not NA:

filter(df, !is.na(x))


`@instructions`


`@hint`


`@pre_exercise_code`

```{r}

```


`@sample_code`

```{r}

```


`@solution`

```{r}

```


`@sct`

```{r}

```


