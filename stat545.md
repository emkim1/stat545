---
title: "stat545"
author: "Emily Kim"
date: "2025-01-16"
output: 
  html_document:   
    theme: united  
    toc: true
    toc_float: true
    keep_md: true  
---



01_github: markdown, html, source code, delimited data, png    
02_basics: R basics, workspace, working directory, RStudio projects

## Intro to STAT 545  
https://daattali.gitbooks.io/stat545-ubc-github-io/content/index.html   
https://speakerdeck.com/jennybc/ubc-stat545-2015-cm001-intro-to-course  

* Introduction to `R` and `RStudio IDE`; scripts, workspace, RStudio Projects  
* Generate reports from R scripts and R Markdown  
* Care and feeding of data in R  
* Data aggregation; "apply: functions, `dplyr`  
* Data visualization with `ggplot2`  
* Graphs and descriptive stats for quantitative and categorical variables  
* Writing R functions  
* Coding style and project organization  
* Version control with Git; collaboration via GitH7b  
* Character data; regular expressions  
* Interactive pages, apps, and graphics with Shiny and ggvis  
* Get data off the web and expose data, code, results on the web  
* Distribute data and code via an R package  
* Automate an analytical pipeline, e.g. with Make  

## Original website   
https://github.com/STAT545-UBC/STAT545-UBC-original-website  newer   
https://github.com/tonydurst/STAT545-UBC.github.io/tree/master  more files. 

## Book on data wrangling, exploration & analysis with R  
https://github.com/rstudio-education/stat545  
https://stat545.com/   

01) Install `R` and `RStudio`. 
02) R basics: scripts, workspace, RStudio Projects  
03) Version control 
04) R Markdown  

05) Care and feeding of data in R  
06) Intro to dplyr  
07) Single table dplyr functions  
08) Tidy data  
09) Writing and reading files  

10) Factors  
11) Character vectors: manipulate, regex regular expressions, stringr  
12) Character encoding  
13) Dates and times  

14) Multiple tibbles: row and column binding, 
15) Joins two tibbles in dplyr  
16) Table lookup  

17) R object indexing  

18-21) Writing R functions  

22) R graphics
23) ggplot2   
24) Effective graphs 
25 - 26) Colors in R  
27) Graphics  
28) Saving figures to file  
29) Multiple plots 

30 - 32) R packages

33) Automate data analysis    
34) Workflow: automate an analytical pipeline  

35) Get Data from the web  
36 - 37) API wrappers  

39) Shiny interactive apps  
40) Appendix  
* Coding style and project organization  

In a wide array of fields the ability to effective process data is superseding classical modes of research.  
"A data scientist is better at statistics than a software engineer and better at software engineering than a statistician"  
[Data science Venn diagram](http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram)  
Data Science = Math & Statistics + Hacking Skills + Expertise

Question > Collect Data > .......
Tidy <> Munge <> Model <> Visualize <> Tidy 
Communicate

## Data analysis 
Data scientists spend 50-80% of their time cleaning a data set, collecting and preparing raw data. 

A picture is worth a thousand words  
Always plot the data. Replace tables of data or statistical results with compelling, accessible figures.  
Generate figures that overlay / juxtapose observed data and analytical results, the 'fit'

Reproducible research, data sharing, documentation  <https://www.youtube.com/watch?v=N2zK3sAtr-4>   

> MD requests data from a researcher, who saved data on a USB drive in hexadecimal format accessible by  Cytosynth program, whose company went bankrupt in 2007.  MD tracked down a copy of the program. In the data set fields were called Sam. The PI remembered that Sam1 is the level of CXCR4 expression. Suggested MD talked to coauthor about other Sam fields, but Sam Lee was back in China.

## RStudio is an IDE integrated development environment for R

RStudio helps: 

* Project organization: knitr, R markdown, R packages  
* Collaboration / Open Science: GitHub   
* Version control / back up: git  

## R Markdown
easy to write / easy to publish

R code is executed and output appears in the document.  
Results are generated on-the-fly  

## Git repository version control      
Write plain text, put it under version control   
Manage files:  writing, coding, data wrangling  

## GitHub = publish Git repositories on the web
Collaboration = the "killer app" of version control
Know the current version, the most recent data   
See how files have changed, when, and by whom  
GitHub issues = "bug tracker" or "to do list"  

GitHub renders Markdown.md files  
Click raw to see the raw Markdown  
GitHub renders .csv and .tsv, comma and tab delimited files

Packages on GitHub: yihui/knitr, hadley/ggplot2, hadley/dplyr  
https://github.com/unorthodox123/RacialDotMap  map of racial segregation    
https://github.com/corynissen/foodborne_classifier analyze tweets to id sources of food poisoning  

## R or Python scripts () to process delimited or structured files 

Raw data (processing code) Analytic data (analytic code) computational results (presentation code)  
Figures, Tables, Numerical Summaries + Text ---> Article  

Jennifer (Jenny) Bryan:  I teach and perform lots of data analysis. 
BA in econ and german, PhD biostatistics, assoc prof @ UBS  
50% statistics / 50% Michael Smith Laboratories  
management consultant  

Class culture  

* teach you to fish (learn from documentation, learning examples, google, stackoverflow)  
* reward engagement, intellectual generosity and curiosity (speak up, share success OR failure, show interest)  
* zero tolerance of plagiarism (generate your own approach, write some code, describe the process). Process is more important than product.  

Goal: work with a data set you choose. Think about datasets you'd like to prepare and analyze.








