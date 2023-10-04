---
title: "Data Tidying Part 1"
output: 
  ioslides_presentation: 
    keep_md: yes
---    
## Tidy data rules
1. Each variable is a column
2. Each observation is a row; each row is an observation
3. Each value is a cell; each cell is a single value

There are advantages to consistency in structuring data. The tidy data approach works particularly well with R functions, which are designed for vectors of values.

Many datasets you'll reuse are NOT tidy because most people aren't familiar with these principles. Data is often organized to make data entry as easy as possible.

## Ways that data can be untidy
- missing values: *explicitly* missing (flagged with NA) or *implicitly* missing (not present in the data)
- data in column names
- observation scattered across multiple rows
- multiple observations in a single column

## Today
We'll get started with coding in R. Create an R script and type along with me - ask questions or let me know if you get an error!
We'll be using untidy datasets to get to know R.
I'll show you the difference between working in R scripts and in an R Notebook.

Key resources: 

- Data Carpentry: see <https://datacarpentry.org/R-ecology-lesson/03-dplyr.html>

- R for Data Science (2e) Chapter 6: see <https://r4ds.hadley.nz/data-tidy>

- R for Data Science (1e) Chapter 12: see <https://r4ds.had.co.nz/tidy-data.html>

## Useful keyboard shortcuts

Executing commands:
In R script file: using *Ctrl+Enter* shortcut in Windows (*Cmd+Enter* on Mac)
In R Notebook: Click on green *Run* button to run code chunk or use *Ctrl+Shift+Enter* (Windows) or *Cmd+Shift+Enter* (Mac)

Assignment operator:
<- *Alt+-* (Windows) or *Option+-* (Mac) 

Pipe:
*Ctrl+Shift+M* (Windows) or *Command+Shift+M* (Mac)

? for help
