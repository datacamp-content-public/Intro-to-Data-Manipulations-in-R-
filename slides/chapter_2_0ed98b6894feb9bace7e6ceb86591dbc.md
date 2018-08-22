---
title: Insert title here
key: 0ed98b6894feb9bace7e6ceb86591dbc

---
## Data Manipulations

```yaml
type: "TitleSlide"
key: "cb448f0e10"
```

`@lower_third`

name: Name Surname
title: Instructor


`@script`



---
##  Some potential issues when manipulating data using Excel:




```yaml
type: "FullSlide"
key: "883bb9005a"
```

`@part1`
- Large datasets in Excel spread sheets can be problematic (e.g. file collapses or it is too slow), specially if the file contains numerous formulas. 
   
- The steps that were followed to produced an output cannot be clearly tracked, so it is is difficult to find out what is wrong or incomplete. 

- Frequently, repetitive operations needs to be done as the data gets updated (e.g. produce new pivot tables).

- If you want to change the layout of your data table, doing so can be quite cumbersome and time-consuming.


`@script`



---
## How R (or other programming languages) can help

```yaml
type: "FullSlide"
key: "ef55d8005f"
```

`@part1`
` ` 

- R is better equipped to handle large amounts of data, so this is a much more efficient solution to dealing with data that would simply cause Excel to freeze up.

- Complex and repetitive time can be automated with a just few lines of code. 
   
- Others (or even yourself) cannot clearly track the steps that were followed to produced an output. 

-Reproducibility. A data analysis needs to be reproducible.
Version control. Good for collaboration and also good for reproducibility. Instead of using xls, use csv (still very complex and has lots of edge cases, but csv parsers are fairly good nowadays.)
Testing. If you don't have tests, your code is broken. If your code is broken, your analysis is worse than useless.


`@script`



---
## Final Slide

```yaml
type: "FinalSlide"
key: "8f5bf7fa48"
```

`@script`


