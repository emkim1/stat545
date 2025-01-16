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



## Start a R Project
Keep all files together: input data, R scripts, analysis results, figures  

RStudio: `File` \> `New Project` \> `Version Control` \> `Git` \> 
Repository URL: https://github.com/emkim1/stat545.git  
`Directory name`: `stat545`  
Create project as a subdirectory of: `/Users/ekim/repo/R`\
√ `Create a git repository` √ `Open in new session` \> `Create Project` 

Add to `.gitignore`:

* .DS_Store  
* .gitignore   

## Start a R Markdown File

`File` \> `New File` \> `R Markdown..`\
`Document` \> `Title` field, `Default Output Format` select `HTML` \> OK

Titles should be similar: `R Markdown` (human) and filename `rmarkdown.Rmd` (computer - no spaces)  

Add to YAML (HTML with md)
output: 
  html_document:   
    theme: united  
    toc: true  
    toc_float: true  
    keep_md: true 

Add to `.gitignore`  

* README.html

### R Markdown

Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. <http://rmarkdown.rstudio.com>.

Click the **Knit** button to generate a document of content and the output of embedded R code.  
`foo.Rmd --> foo.md --> foo.html`

