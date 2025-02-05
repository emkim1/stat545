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
https://speakerdeck.com/jennybc/happy-git-and-github-for-the-user  

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

## GitHub repo files are browsable
<https://daattali.gitbooks.io/stat545-ubc-github-io/content/bit006_github-browsability-wins.html>

Inspect GitHub repository files in a browser. 
Special handling for:  

* Markdown files    
* `README.md` Markdown files  
* HTML files, compiled from Markdown files  
* Source code: `.R` files
* Delimited data files: .csv (comma-separated), .tsv (tab-separated)
* PNG files   
* vector-based PDF files are slower     

## RStudio Project  
* a directory on your computer  
* make that an RStudio Project: save changes      
* make that a Git repository: commit changes     
* push to GitHub periodically   

make commits, view history and diffs, push to /pull from GitHub


## R Markdown   
`Knit` markdown with button OR command line  
```
library(rmarkdown)
render("foo.Rmd")
```
https://speakerdeck.com/jennybc/happy-git-and-github-for-the-user?slide=56  

R Markdown --> Markdown --> HTML  
`foo.Rmd --> foo.md --> foo.html` 
easy to write / easy to publish   
---   
title: "Untitled"   
output:  
 html_document:   
 keep_md: yes.  
---   

R Markdown --> Markdown  
`foo.Rmd --> foo.md`  
easy to write / easy to GitHub   
---   
output:   
 md_document  
___   

Commit `foo.Rmd` and `foo.md`  
.gitignore `foo.html` 

## R

R --> Markdown --> HTML  
`foo.R --> foo.md --> foo.html` 
easy to write / easy to publish   
---   
title: "Untitled"   
output:  
 html_document:   
 keep_md: yes  
---   

R --> Markdown  
`foo.R --> foo.md`  
easy to write / easy to GitHub   
---   
output:   
 md_document  
___   

## README.md  
`README.md` is the landing page for each directory  
Examples:  
Data cleaning: https://github.com/jennybc/gapminder/tree/main/data-raw  
How to share data with a statistician https://github.com/jtleek/datasharing  
PNG README: https://github.com/kbroman/FruitSnacks/blob/master/PhotoGallery.md  
PNG REAMDE: https://gist.github.com/jennybc/0239f65633e09df7e5f4

## HTML  
GitHub shows the raw HTML  
Replace `https://github.com/` with `https://rawgit.com/` to render the HTML  

## Links and embedded figures  
`[emkim1](directoryName/)` will link to the `directoryName/` directory in the repo  
`![](image.png)` will include `image.png` in the current directory

## Find files on GitHub  
https://github.com/tonydurst/STAT545-UBC.github.io/blob/master/bit006_github-browsability-wins.md  

* Press `t` to activate the file finder when in directory view. Finds files in subdirectories.  
* Press `y` to get a permanent link when viewing a specific file. Watch what changes in the URL. This is important if you link to a file or to specific lines. Otherwise your links will break easily in the future. If the file is deleted or renamed or if lines get inserted or deleted, your links will no longer point to what you intended. Use `y` to get links that include a specific commit in the URL.

GitHub maximum file size is 50 MB, repository max is 1-5 GB  
<https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github>


