---
title: "02_basics"
author: "Emily Kim"
date: "2025-01-20"
output: 
  html_document:   
    theme: united  
    toc: true  
    toc_float: true  
    keep_md: true 
---



## RStudio

Default panes:  

* Console  
* Environment/History  
* Files/Plots/Packages/Help  

Keyboard shortcuts: `option`+`shift`+`K`

Quit RStudio: `command`+`Q` or `q()` in Console ⌘Q

## R Objects

Create objects with the operator `<-`  

* `option` + `-` in Console    
* give the object an assignment:  "objectNames gets value"  
```
objectName <- value
```
Object names:   

* Can NOT start with a digit. 
* Can NOT contain a comma or space.  

Demarcate words:  

* snake_case
* use.periods
* CamelCase

Object appear in the workspace Environment  

* List objects: `objects()` or `ls()` 
* Remove object `y`: `rm(y)`
* Remove everything: rm(list=ls()) or click broom in Environment tab

## R functions 
```
functionName(arg1 = val1, arg2 = val2, and so on)
```
Specify `argument = value` or input argument by position  

Functions: Type part of name and hit TAB. Floating help shows arguments. F1 shows full documentation.  
`seq()` makes sequences of numbers  
Type `se` and hit `Tab` to see possible completions. Specify `seq` by typing more or using up/down arrows.  
Type opening parenthesis:  auto adding of closing parenthesis, cursor placed in middle  
Type `1,10` and hit return to exit the expression.   
```r
seq(1,10)
```
R assumes `from = 1` and `to = 10` and `step = 1`

Surround assignment with parentheses to "print to screen"  
```
(y <- seq(1,10)))
```
Some functions don't require arguments 
```r
date()
```

## RStudio Project
All project files - input data, R scripts, analytic results, figures  
Open project, check working directory
```r
getwd()
```
Enter some commands in the Console:
```
a <- 2
b <- -3
sig_sq <- 0.5
x <- runif(40)
y <- a + b * x + rnorm(40, sd = sqrt(sig_sq))
(avg_x <- mean(x))
```
Plot result
```
write(avg_x, "avg_x.txt")
plot(x, y)
abline(a, b, col = "purple")
```
Save output as pdf
```
pdf("my_plot.pdf") # open device
plot(x,y)
abline(a,b, col = "purple")
dev.off() 
```
Paste the code into `Source`: `History` /> `To Source` 

* Save the code as R script `.R` or `.r`  
* Save the code as Rmd `.Rmd`  
* Quit and Restart RStudio  

Edit code and output  

* Set the sample size `n` at the top, replace hard-wired 40's with `n`     
* Run the code line-by-line `command + enter`  
* Run several lines: Highlight and hit `Run`  
* Source the entire document
  * `shift`+`command`+`S`  
  * `source('toy-script.r') in Console  
  * mouse /> Source in Console of `.R` file
```
n <- 40 # set sample size
a <- 2
b <- -3
sig_sq <- 0.5
x <- runif(n)
y <- a + b * x + rnorm(n, sd = sqrt(sig_sq))
(avg_x <- mean(x))

pdf("my_plot.pdf",         # File name
    width = 8, height = 7, # Width and height in inches
    bg = "white",          # Background color
    colormodel = "cmyk",    # Color model (cmyk is required for most publications)
    paper = "A4")          # Paper size
plot(x,y)
abline(a,b, col = "purple")
dev.off()
```


