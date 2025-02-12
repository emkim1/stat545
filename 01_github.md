---
title: "01 GitHub"
author: "Emily Kim"
date: "2025-01-21"
output: 
  html_document:   
    theme: united  
    toc: true
    toc_float: true
    keep_md: true  
---



https://happygitwithr.com/  last update 2020  
https://happygitwithr.com/rmd-test-drive 
https://speakerdeck.com/jennybc/ubc-stat545-2015-cm001-intro-to-course
https://speakerdeck.com/jennybc/happy-git-and-github-for-the-user  

## ## STAT 545 Episode 2A: Git and GitHub for an Organized Project
https://www.youtube.com/watch?v=l2ftm-YwJs8  

1) Use cloud-based storage as your official project storage 
2) Use cloud version control   
  Track changes to your analysis.    
   See how a project came to be: previous versions     
3) Use computer version control:  what & when to track and sync with the cloud.  
  `Pull` from cloud (1st time is a clone)  
  `Push` to cloud to update with computer  
* Git treats the cloud-based service as the official version of the project  
  `Pull` before `Push` = update the local version, before you update the cloud version    
* `Commit`:  track local changes to your work since the last commit. 
  A GitHub project is a stack of commits, called a Commit History         
  `commits` on GitHub show the Commit History. Look at a particular file, to see who contributed to what and when.   
4) Use Pull Requests to review changes. Team review before incorporating changes into the official version.  
  Work on a branch, push branch to GitHub , open a pull request `Compare & pull request`
  See where collaborators made changes, comment on those changes  
5) Use Issues to communicate with your team:  like a project discussion board. Tag a teammate will notify them.
  
RStudio has a Git tab as a Git client  

## GitHub Account  
https://github.com > sign up uniklinik      
emkim1 / g11

## Git installed ?   

Git installed, but ...  
$ git
$ which git   
`/usr/bin/git`   
$ git --version   
`xcrun: error: invalid active developer path`  

Xcode installed, but ...   
Check Xcode
$ xcode-select --version  `  
`xcrun: error: invalid active developer path` 

Install Xcode Command Line Tools ~130 MB, not entire Xcode  
$ xcode-select --install	> Install > Agree (must agree to license agreement)

Xcode & Git installed & work:           
$ xcode-select --version   
`xcode-select version 2395.`  
$ clang --version
`Apple clang version 14.0.0 (clang-1400.0.29.202)`  
$ git --version  
`git version 2.37.1 (Apple Git-137.1)`  


## RStudio is an IDE integrated development environment for R

* Project organization: knitr, R markdown, R packages  
* Collaboration / open science: GitHub   
* Version control / back up: git  

## RStudio Project  
* a directory on your computer  
* make that an RStudio Project: save changes      
* make that a Git repository: commit changes     
* push to GitHub periodically   

make commits, view history and diffs, push to /pull from GitHub

## Markdown

Markdown --> HTML  
`foo.Rmd --> foo.html` 
easy to write / easy to publish and read in browser   

## R Markdown   
R code is executed (on-the-fly) and output appears in the document.  

R --> Markdown --> HTML  
`foo.R --> foo.md --> foo.html` 
easy to write / easy to publish and read in browser   

## Git = repository version control        
Manage files: for writing, coding, data wrangling 
Write plain text, put it under version control   

## GitHub = host Git repositories on the web
Keep track of files: see the current version, the most recent data   
Diff view = see exactly what changed, when, and by whom  
Commit message = why changed  
Issues = bug reports, feature requests, to do list  
Pull requests = mechanism to propose, discuss and merge changes into a repository  

## GitHub renders files nicely   

* Markdown files: .md, click raw to see raw Markdown    
* Delimited data files: .csv (comma-separated) .tsv (tab-separated)

* `README.md` Markdown files  
* HTML files, compiled from Markdown files  
* Source code: `.R` files
* PNG files   

## GitHub = publish Git repositories on the web

Open source packages on GitHub: yihui/knitr, hadley/ggplot2, hadley/dplyr  
https://github.com/unorthodox123/RacialDotMap  map of racial segregation    
https://github.com/corynissen/foodborne_classifier analyze tweets to id sources of food poisoning  

## Makefile: R or Python scripts () to process delimited or structured files 
GNU Make can keep complicated software in sync. Originally used to compile software. Now used to express what depends on what, to keep things in sync.    

Raw data -(processing code)-> Analytic data -(analytic code)-> computational results -(presentation code)-> Figures, Tables, Numerical Summaries --> Article  <-- Text

How to make results reproducible and up-to-date ?  
If data changes, how do remember to remake figures 2B and 4 ? 



