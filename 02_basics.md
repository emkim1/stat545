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



https://stat545.com/r-basics.html  

https://daattali.gitbooks.io/stat545-ubc-github-io/content/cm002_r-rstudio-intro.html  
https://daattali.gitbooks.io/stat545-ubc-github-io/content/block002_hello-r-workspace-wd-project.html  

### STAT 545 Episode 1A: Coding your Data Analysis for Success  
https://www.youtube.com/watch?v=91LmBj29-Sc  

1) Save your code: writing code is different than running code  
2) Use an IDE to write code: write & execute code in the same program  
3) Apply functions to your data: turn data into an object, apply functions to get results (graphs, tables, models).  
A function does not change the original object:  store the output of the function in a new variable  
4) Start with a clean slate: run code from top to bottom   
5) Use add-on packages to expand functionality:  `install.packages("dplyr")` run once.  
Load a package to use its functions: `library()` run at top of script  

### RStudio
https://happygitwithr.com/install-r-rstudio  

IDE integrated development environment  

Default panes:  

* Console (left): execute code  
* Environment/History (upper right)  
* Files/Plots/Packages/Help (lower right) 

Keyboard shortcuts: `option`+`shift`+`K`

Quit RStudio: ⌘Q or `q()` in Console  

### R Objects
```
objectName <- value
```
Assign an object a value, with operator `<-`  

* `option` + `-` in Console    
* "objectNames gets value"    

Object names:   

* Can NOT start with a digit. 
* Can NOT contain a comma or space.  

Demarcate words:  

* snake_case
* use.periods
* CamelCase

### R functions 
```
function(arg1 = val1, arg2 = val2, and so on)
seq(1,10)
```
Specify a function: `argument = value` or by position  
Type part of name and hit TAB. Floating help shows arguments. F1 shows full documentation.  

`seq()` makes sequences of numbers  

1) Type `se` and hit `Tab` to see possible completions 
2) Specify `seq` by typing more or using up/down arrows  
3) Type opening parenthesis:  auto adding of closing parenthesis, cursor placed in middle  
4) Type `1,10` and hit return to exit the expression   
5) R assumes `from = 1` and `to = 10` and `step = 1` 

Surround the assignment with parentheses to "print to screen"  
```
(y <- seq(1,10)))
```
Certain functions don't need arguments 

``` r
date()
```

```
## [1] "Tue Feb 11 12:50:25 2025"
```

### Workspace

Objects appear in the workspace Environment

* List objects: `objects()` or `ls()` 
* Remove object y: `rm(y)`
* Remove everything: `rm(list=ls())`   
* or click the broom in Environment pane  

Save workspace: `Save workspace image to ~/.Rdata`  

### Source code  
Save your analysis as R scripts: `.R` or `.r`  
Store scripts for every object in an easy-to-find directory   
Redo your analysis with input data and R code. Reuse your code    

Scripts  
* `#` to comment `command + shift + C`  
* Write code for humans, write data for computers  
* Files names: `number_clear-description.filetype`  
* Dates: `yyyy-mm-dd_clear-description.filetype`  

### Working directory  
```r
getwd()
setwd("~/ekim/R/repo/R/stat545")
```
Organize your projects into directories. Set the working directory to the project directory.  

Where R looks for files to load. Where R writes files to disk.  
Check working directory or set working directory  

### Workflow

* Create an RStudio project for a project  
* Keep inputs there (for importing), load using code, NOT the mouse       
* Keep scripts there; edit them, run them in bits or as a whole from there
  * Load data or save a figure using code    
* Keep outputs there (like the PDF written above), save using code, NOT the mouse  

Clean workspace with broom or `rm(list=ls())`  
Restart R to re-run analysis to ensure that code is complete/correct   

### RStudio Project
All project files - input data, R scripts, analytic results, figures  
Open project to set working directory  

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
This is a good start, so let's preserve the logic and code.  
`History` > `To Source` to paste the code into `Source` as a new R script     
Save the code as R script `.R` or `.r`  or Rmd `.Rmd`  
`#` to comment `command + shift + C`  
Quit and inspect project folder. View the PDF.  

Restart RStudio  
Edit code  

* Set the sample size `n` at the top, replace hard-wired 40's with `n`  
* Alter the sample size `n`, the slope of line `b`, the color of the line  

Re-run code

* Walk through line-by-line `command + enter` 
* Run several lines `Run` > `Run Selected Line(s)`  
* Source the entire `.Rmd`
  * `shift`+`command`+`S` or  `Run` > `Run All`
* Source entire `.R`  
  * `source('toy-script.r')` in Console  
  * mouse > Source  
  
Visit your figure in an external viewer to verify that the PDF is changing as expected  
Find the script that created the PDF  

```
# Add {r} to this code to run  
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
 
