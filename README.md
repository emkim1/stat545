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
https://happygitwithr.com/new-github-first.html 

## Start a R Project, GitHub first  
Keep files together: input data, R scripts, analysis results, figures  
This new sub-directory `stat545` serves as:

* a remote GitHub repository linked to a local Git repository    
* an RStudio Project  
* a directory on your computer

1) GitHub: make a repo  
`Repositories` > `New`  
* Repository name: `stat545`  
* Private
* Initialize with: Add `README file`  
`Create repository` > click `<> Code`  
Copy the clone repository HTTPS URL  <https://github.com/emkim1/stat545.git>  

2) RStudio: start a new project    
`File` > `New Project` > `Version Control` > `Git`  

* Repository URL: <https://github.com/emkim1/stat545.git>  
* Directory name: `stat545`  
Create project as a sub-directory of: `/Users/ekim/repo/R`  
√ `Open in new session` > `Create Project` 

3) Add to `.gitignore`:

* .DS_Store  
* .gitignore
* .README.html 

4) Look for the `README.md` file from GitHub  
Workflow: Edit `README.md`, Commit, Push to GitHub  

* click `Git` tab  
* check `Staged` box for files to commit  (Diffs show what changed since last commit)  
* click `Commit`  
* type a Commit message = short description of what/why changed    
* click `Commit`  
* Pull from GitHub  
* Push to GitHub after a couple of commits  
* Check change on GitHub  

## Start a R Markdown File
<https://daattali.gitbooks.io/stat545-ubc-github-io/content/block007_first-use-rmarkdown.html>
https://happygitwithr.com/rmd-test-drive  

`File` > `New File` > `R Markdown..`
`Document` > `Title` field, `Default Output Format` select `HTML` > OK

Titles should be similar: `R Markdown` (human) and filename `rmarkdown.Rmd` (computer - no spaces)  

1) YAML output format (HTML with md)  

* Click Gear > `Output Options` > General > Include TOC, Depth of header 3, Apply theme `united`  
Advanced > `Keep markdown source file`  
* Or hand-edit:  
output: 
  html_document:   
    theme: united  
    toc: true  
    toc_float: true  
    keep_md: true 
    
    Delete cars code, pressure plot

2) Add to `.gitignore`  

* rmarkdown.html

3) Workflow:  
RStudio: `Pull` (when collaborate) \> Edit locally and save \> `Stage` \> `Commit` \> `Push`  
* Knit to generate `README.html
* `.Rmd` and `.md`: Stage, Commit and Push

## R Markdown

Markdown is a simple formatting syntax for authoring HTML, PDF and MS Word documents. <http://rmarkdown.rstudio.com>.
Click the **Knit** button to generate a document of content and the output of embedded R code.  
`foo.Rmd --> foo.md --> foo.html`

Write a paper - intro, methods, results, discussion, conclusion - with the code for each section  
Entire pipeline in an R Markdown document: data processing, analysis, outputs, visualization
Figures update when code parameters change  

## Formatting

### Blockquote

`>` to indent

### Bullet point

### Font

*italic*  `*italic*` or `_italic_`  
**bold**  `**bold**` or `__bold__`  
***italic bold***   `***italic bold***` or `___italic bold___`  
<s>strikethrough</s>  `<s>strikethrough</s>`  
`verbatim` \``verbatim` \`        
text^super^  `text^super^`  
text~sub~  `text~sub~`

### Section Header

`#`, then a space before the header text (`#` Biggest, `######` Smallest)

### Equation & Symbol

#### Inline equation: 
the average is computed as $\frac{1}{n} \sum_{i=1}^{n} x_{i}$  

#### Display equation:
$$
\begin{equation*}
|x|= 
\begin{cases} x & \text{if $x≥0$,} \\\\
-x &\text{if $x\le 0$.}
\end{cases}
\end{equation*}
$$

#### Symbol: 
$\sigma$ `$\sigma$`  to render as TeX Math, enclose by `$`  

