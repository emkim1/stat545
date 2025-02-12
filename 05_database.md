---
title: "05_database"
author: "Emily Kim"
date: "2025-01-22"
output: 
  html_document: 
    toc: true
    toc_float: true
    keep_md: true
    theme: united
    number_sections: true
---



## Basic care and feeding of data in R  
https://daattali.gitbooks.io/stat545-ubc-github-io/content/block006_care-feeding-data.html

## Clear workspace
Ensure that the code you write is complete and re-runnable.  
Return to a clean slate often, to avoid hidden dependencies on hidden objects or packages.  

Broom icon in Environment or `Session > Clear Workspace` or `rm(list=ls())` in Console  
Restart R to unload packages:  `Session > Restart R` or q() and relaunch 
Open a new R script  


``` r
# install.packages("gapminder")
library(gapminder)
```

A Data.frame is a list. 
Like a matrix, the length of each list component is the same.    
Unlike a matrix, vector types can differ (numeric, character, categorical)   

str() structure of the data.frame   
head() first 6 rows, tail() last 6 rows

Basic info  
names()  
ncol(), nrow(), length()  

Statistical overview: 
summary()  

When coding: 
Work with data.frame arguments to pass data to functions     
data =   
subset = to restrict data  
if a function lacks certain arguments, use with() 
eg. with(subset(gapminder, subset = country == "Colombia"),
cor(lifeExp, gdpPercap))

Give variables short informative names (lifeExp versus X5) for downstream figures, tables  
Refer to variables by name, not column number  
Code is self-documenting and robust  

Visualization:  
plot(lifeExp ~ year, gapminder)  
plot(lifeExp ~ gdpPercap, gapminder), plot(lifeExp ~ log(gdpPercap), gapminder)  

Use `$` to specify the numeric variable for life expectancy  
head(gapminder$lifeExp)  
summary(gapminder$lifeExp)  
hist(gapminder$lifeExp)  

Use `$` to specify the numeric variable for year, which functions like a categorical variable.  
summary(gapminder$year)  
table(gapminder$year)   

Categorical variables for continent are stored as a factor  
```
class(gapminder$continent) = factor  
summary(gapminder$continent) 
levels(gapminder$continent) # [1] "Africa"   "Americas" "Asia"     "Europe"   "Oceania"  
nlevels(gapminder$continent) # [1] 5  factors are coded as integers 1-5  
table(gapminder$continent) # number of observations for each continent  
#  Africa Americas     Asia   Europe  Oceania 
#     624      300      396      360       24 
barplot(table(gapminder$continent)) 

```

subset() the observations   
subset(gapminder, subset = country =="Uruguay")  

## R objects beyond data.frames    
https://daattali.gitbooks.io/stat545-ubc-github-io/content/block004_basic-r-objects.html  

## Vectors  

Assign a vector a value with shortcut `Option + -` 

x <- 3*4  
is.vector(x)  
length(x) # 1  

Index vectors with square brackets.  

x[2] <- 100  
x # 12 100 
x[5] <- 3  
x # 12 100 NA NA 3  
x[11] # NA  
x[0] # numeric(0)  

R recycles vectors if not the necessary length.  

c() catenate function to make vectors  

str(c("hello", "world")) # chr [1:2] "hello" "world"

Atomic vectors 
Hold the same type of variables, coercing elements if necessary  
* logical: easily coreced into 1's and 0's
* numeric  
* character  

Index a vector  

* logical vector: keep elements associated with TRUEs, ditch the FALSEs
* vector of positive integers specifying the keepers
* vector of negative integers specifying the losers
* character vector, naming the keepers  

## Lists  
Like a vector, with different elements  

* data.frames are lists, where each element is an atomic vector, all the same length  
* function that return lists, that you want to extract, such as p-value for hypthesis test  

a <- c("cabbage", pi, TRUE, 4.3) # [1] "cabbage"  "3.14159265358979" "TRUE" "4.3"  
(a <- list("cabbage",pi,TRUE, 4.3))
str(a)
List of 4  
 $ : chr "cabbage"  
 $ : num 3.14  
 $ : logi TRUE  
 $ : num 4.3   
 
 Add names to a list

