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

Normally, people write their codes in a "Script.R" file, which is equivalent to a text file. That allows the user to save their code to work on it later on.  

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
# Write your code here
```


`@solution`

```{r}
2+2
```


`@sct`

```{r}
4
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
___ <- ___


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


nrows
ncol
head
names


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


