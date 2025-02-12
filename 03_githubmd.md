---
title: "03 GitHub md"
author: "Emily Kim"
date: "2025-01-22"
output: 
  html_document:   
    theme: united  
    toc: true
    toc_float: true
    keep_md: true 
---



https://speakerdeck.com/jennybc/happy-git-and-github-for-the-user

## RStudio with Git and GitHub  
Use RStudio as a Git(Hub) client.  
Git pane: make commits, view history and diffs, push to /pull from GitHub

### RStudio Project  
* a directory on your computer  
* make that an RStudio Project: save changes      
* make that a Git repository: make commits       
* push to GitHub periodically   

### Git 
Version control system = originally to manage files for software development  
Repurposed for writing, coding, data wrangling 

### (R) Markdown + Git(Hub)

Presentable, web-friendly version of R and Rmd files. 

easy to write / easy to read  
`foo.R ----> foo.md`  
`foo.Rmd --> foo.html` 

### Markdown 

Markdown --> HTML  
`foo.md --> foo.html`  
easy to write / easy to publish  

Markdown -->   
`foo.md --> `     
GitHub renders Markdown like HTML: but not code  

### R Markdown + Git(Hub)  

R Markdown ---> Markdown  
R code is executed (on-the-fly) and output appears in the markdown document  

Markdown ---> HTML  
Markdown is rendered into HTML    

R Markdown --> Markdown --> HTML  
`foo.Rmd --> foo.md --> foo.html`  
easy to write / easy to publish   

R Markdown --> Markdown  
`foo.Rmd --> foo.md`  
easy to write / easy to GitHub  

`Knit` markdown with button OR command line  
```
library(rmarkdown)
render("foo.Rmd")
```

### R Markdown: 
YAML header: specify the output when rendering an Rmd document      

R Markdown --> HTML  
`foo.Rmd --> foo.html`   

---   
title: "Untitled"   
output: html_document   
---

R Markdown --> Markdown --> HTML  
`foo.Rmd --> foo.md --> foo.html`   
---   
title: "Untitled"   
output:  
 html_document:   
 keep_md: yes  
---   

R Markdown --> Markdown  
`foo.Rmd --> foo.md`  
---   
output:   
 md_document  
___   

R Markdown --> Markdown  
`foo.Rmd --> foo.md`  
---   
output:   
 github_document  
___   


### R: 
YAML header: specify the output when rendering an R script    

R script --> HTML  
`foo.R --> foo.html` 
#' ---   
#' title: "Untitled"   
#' output: html_document   
#' ---

R script --> Markdown --> HTML  
`foo.R --> foo.md --> foo.html` 
#' ---   
#' title: "Untitled"   
#' output:  
#'  html_document:   
#'  keep_md: yes  
#' ---   

R script --> Markdown  
`foo.R --> foo.md`  
#' ---   
#' output:   
#'  md_document  
#' ___   

R script  --> Markdown  
`foo.R --> foo.md`  
#' ---   
#' output:   
#'  github_document  
#' ___   

### RStudio Rmd with Git and GitHub  
https://happygitwithr.com/rmd-test-drive.html

Your project can be both machine & human readable  

One definitive source for rendered files:  
.Rmd --> .R .md .html   

Commit both markdown files: `foo.Rmd` and `foo.md`  
`.gitignore` `foo.html` 

Workflow:  
* make markdown  
* commit markdown  
* Rmd -> markdown or R -> markdown  
output_format: github_document  

Change something, render, commit, push, repeat    

### GitHub repo files are browsable
https://happygitwithr.com/repo-browsability.html
<https://daattali.gitbooks.io/stat545-ubc-github-io/content/bit006_github-browsability-wins.html>

Get a pseudo website for free. Inspect GitHub repository files in a browser. 
Files that are well rendered in GitHub:  

* Markdown files    
* `README.md` Markdown files  
* HTML files, compiled from Markdown files  
* Source code: `.R` files
* Delimited data files: .csv (comma-separated), .tsv (tab-separated)
* PNG files   
* vector-based PDF files are slower   

GitHub renders Markdown.md files. Click raw to see the raw Markdown  
- code can be machine & human readable  
GitHub renders .csv and .tsv, comma and tab delimited files  
- data can be machine & human readable  

## README.md  
`README.md` is the landing page for each directory  
Data cleaning: https://github.com/jennybc/gapminder/tree/main/data-raw  

## GitHub = track files  
What is here? When did it last change? Who changed it? Why?  
Commits are how files evolve  
Commit message = short description of what / why changed  
Diffs = show what changed, when, and by whom  
Issues = bug reports, feature requests, to do list  

Collaboration = the "killer app" of cloud version control  
Pull requests = mechanism to propose, discuss and merge changes into a repository  

## Find files on GitHub  
https://github.com/tonydurst/STAT545-UBC.github.io/blob/master/bit006_github-browsability-wins.md  

* Press `t` to activate the file finder when in directory view. Finds files in subdirectories.  
* Press `y` to get a permanent link when viewing a specific file. Watch what changes in the URL. This is important if you link to a file or to specific lines. Otherwise your links will break easily in the future. If the file is deleted or renamed or if lines get inserted or deleted, your links will no longer point to what you intended. Use `y` to get links that include a specific commit in the URL.

## HTML  
GitHub shows the raw HTML  
Replace `https://github.com/` with `https://rawgit.com/` to render the HTML  

## Links and embedded figures  
`[emkim1](directoryName/)` will link to the `directoryName/` directory in the repo  
`![](image.png)` will include `image.png` in the current directory

GitHub maximum file size is 50 MB, repository max is 1-5 GB  
<https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github>
