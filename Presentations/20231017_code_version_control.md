Code documentation & version control
================
Elizabeth Stregger
2023-10-16

## Current location in the research lifecycle

We’ve arrived at the process / analyze / interpret data step

Data management tasks include:

- version control

- document code & processes

## Last class:

Version control for shared documents:

- save working files at key points

- save files with a new version number before editing

- include a version number at the end of the file name

- keep notes on what the version contains

- consider: controlling write access to important versions so they are
  not accidentally overwritten

## But… we’re using GitHub!

This class, we’ll talk about code style in RStudio and version control
in GitHub.

## Code style

Resource: R for Data Science (2e)
<https://r4ds.hadley.nz/workflow-style>

Resource: Tidyverse Style Guide <https://style.tidyverse.org/index.html>

We’re using tidyverse and nycflights13 packages for code examples.

First, install nycflights13 package in the console.

Reminder on how to install packages: install.packages(“nycflights13”)

``` r
# library(tidyverse)
# library(nycflights13)
```

## Before we start talking style, get to know the data

``` r
# What are some of the functions we can use to get to know the flights dataset?
# head(flights)
# ?flights
# str(flights)
```

## Names

Variable names should only use:

- lowercase letters

- numbers

- underscores

## Tips for names

- Long descriptive names are better than short ones.

- Use tab to autocomplete when you’re reusing variables.

- Try to be consistent about names.

- Better to have a common prefix than suffix

``` r
# Strive for:
# flights_short <- flights |> 
#  filter(air_time < 60)

# Not so great names:
# SHORTFLIGHTS
# ShortFlights
# short_flights
```

## Spaces

- Include spaces on either side of mathematical operators (except ^)
- Always put a space after a comma, just like in writing text.
- Do not put spaces after regular function calls or the \$

``` r
# Strive for:
# mean(flights$air_time, na.rm = TRUE)

# Not so great spacing (still works):
# mean (flights$air_time,na.rm=TRUE)
```

## Pipes

- \|\> should always have a space before it

- Line break after the pipe makes it easier to follow the logic of the
  code

- Put each named function on a new line

``` r
# strive for:
#flights |> 
#  filter(!is.na(arr_delay), !is.na(tailnum)) |> 
#  count(dest)

# not so great:
# flights|>filter(!is.na(arr_delay),!is.na(tailnum))|>count(dest)
```

## Sectioning comments in scripts

Use sectioning comments to break up your file into manageable pieces.

RStudio shortcut: Cmd/Ctrl + Shift + R

## Styler package

- Styler package by Lorenz Walthert
  <https://www.tidyverse.org/blog/2017/12/styler-1.0.0/>

- Based on Tidyverse Style Guide
  <https://style.tidyverse.org/index.html>

Use from RStudio Add-ins

## Assignment: Update Week 5 code

In RStudio, open the script file you deposited with week 5 code.

Install the styler package if you have not already installed it. Agree
to any pop-up messages about changes.

Using the styler addin, choose “style active file” and save the file.
Commit and push the file to GitHub. Look at the file versioning to see
if there are any changes.

## Git concepts and definitions

Source: Happy Git and GitHub for the useR
<https://happygitwithr.com/git-basics>

Repository: directory of files that Git manages

Commit: functions like a snapshot of files in a repository

Diff: the differences between committed versions

Including a useful commit message helps you identify versions or the
steps in a project.

## Working with others in Git

- We’ve been working in personal repositories, so we haven’t had any
  conflicting versions.

- Conflicts happen if two people are working on the same file(s) at the
  same time.

- Best option: create a branch and merge it later
