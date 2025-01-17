---
title: "readme"
author: "Emily Kim"
date: "2025-01-16"
output: 
  html_document:   
    theme: united  
    toc: true
    toc_float: true
    keep_md: true  
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE) # expose your code, use FALSE sparingly
```

## Start a R Project, GitHub first
Keep files together: input data, R scripts, analysis results, figures  

1) GitHub: create a new repo  
<https://github.com> `Repositories` \> `New`  
* Repository name: stat545  
* Private
* Initialize with: Add README file
`Create repository` \> click `<> Code`  
Clone/Copy repository HTTPS URL: <https://github.com/emkim1/stat545.git>  

2) RStudio: create a new project using the new GitHub repo
`File` \> `New Project` \> `Version Control` \> `Git` \>  

Repository URL: <https://github.com/emkim1/stat545.git>  
`Directory name`: `stat545`  
Create project as a subdirectory of: `/Users/ekim/repo/R`\
√ `Open in new session` \> `Create Project` 

3) Add to `.gitignore`:

* .DS_Store  
* .gitignore   

4) Edit READ.me, commit, push to GitHub  

5) Workflow:  
Pull (if collaborate) \> Make changes (and save) \> Stage \> Commit \> Push  

GitHub maximum file size is 50 MB, repository max is 1-5 GB
<https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github>

## Start a R Markdown File

`File` \> `New File` \> `R Markdown..`\
`Document` \> `Title` field, `Default Output Format` select `HTML` \> OK

Titles should be similar: `R Markdown` (human) and filename `rmarkdown.Rmd` (computer - no spaces)  

1) Add to YAML (HTML with md)
output: 
  html_document:   
    theme: united  
    toc: true  
    toc_float: true  
    keep_md: true 

2) Add to `.gitignore`  

* README.html

### R Markdown

Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. <http://rmarkdown.rstudio.com>.

Click the **Knit** button to generate a document of content and the output of embedded R code.  
`foo.Rmd --> foo.md --> foo.html`

