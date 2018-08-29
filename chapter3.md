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
# Subset those columns starting with 'd' and store it in a new object called 'variables'. 
```


`@solution`

```{r}

```


`@sct`

```{r}

```


