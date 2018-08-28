---
title: 'Chapter 1: R Basics'
description: ""
---

## R Basics / Entering commands

```yaml
type: NormalExercise 
xp: 100 
key: 2fff329b50   
```


R is a command line driven program. It means that you enter your commands at a prompt (R Console), and an output is produced after you press "Enter".

Normally, people write their codes in a "Script.R" file, which is equivalent to a text file. That allows the user to save their code to work on it later.  

In the right hand side, you can see both the _Sript.R_ file, and the _R Console_. You can write your code in the _Srcipt.R_ window and see the output of your code in the _R Console_ by pressing the button **Run Code.**


`@instructions`
Please write the following command in the Script.R window and see the output in your R Console:

`` 2+2 ``

Once you see the output press **"Submit Answer"**

`@hint`


`@pre_exercise_code`

```{r}

```


`@sample_code`

```{r}
# Write your code below
___ + ___
```


`@solution`

```{r}
2+2
```


`@sct`

```{r}

```


`@possible_answers`


`@feedback`


---

## Creating a new variable

```yaml
type: NormalExercise 
xp: 100 
key: 5a775cde05   
```


You can use the assignment operator ( <- ) to create new variables.

For instance, you can create a new object called "four" which will be equal to 2+2:

`four <- 2+2`


`@instructions`
Please create a new object called _five_, which is the result of dividing ten between two.

Then, type _five_ and run the code to evaluate your new object.

`@hint`
The operator for divisions is ( / ). For instance dividing four by two would be `4/2`

`@pre_exercise_code`

```{r}

```


`@sample_code`

```{r}
# Define new object called five:



# Evaluate your new object
```


`@solution`

```{r}
five <- 10 / 2
five
```


`@sct`

```{r}
ex() %>% check_object("five") %>% check_equal(5)
success_msg("amazing!")
```


---

## Explore data

```yaml
type: NormalExercise 
xp: 100 
key: 5587700676   
```


We have created a new object called `cars`. It contains a table (or dataframe as it is called in R) with information about different cars.

You can explore the first 6 records contained in the object `cars`, by using the function:
`head()`


`@instructions`
Explore the layout of the object `data` using the function `head()`

`@hint`
To explore a dataframe called 'x' you would use `head(x)`

`@pre_exercise_code`

```{r}
cars<-mtcars
```


`@sample_code`

```{r}
# Explore object 'data' using the function head()

```


`@solution`

```{r}
head(cars)
```


`@sct`

```{r}

```


---

## Insert exercise title here

```yaml
type: MultipleChoiceExercise 
xp: 50 
key: 6f1a42095c   
```


Other useful options to explore a dataframe are:

- `nrow()`  return the number of records (rows)
- `ncol()`  return the number of columns (variables)
- `names()` return the names of the columns (variables) 

Please indicate how many cars (records) appear in the object 'data':


`@instructions`
- 25 cars
- 28 cars
- 32 cars

`@hint`
Use the function `nrow()` to explore the cumber of cars.

`@pre_exercise_code`

```{r}
cars<-mtcars
```


`@sct`

```{r}
test_output_contains("25 cars", incorrect_msg = "Incorrect answer. Try again")
test_output_contains("28 cars", incorrect_msg = "Incorrect answer. Try again")
success_msg("Correct!)
```


---

## Insert exercise title here

```yaml
type: MultipleChoiceExercise 
xp: 50 
key: 53b2aa63dc   
```





`@instructions`


`@hint`


`@pre_exercise_code`

```{r}

```


`@sct`

```{r}

```


