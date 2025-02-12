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



## STAT 545 Current  
https://stat545.stat.ubc.ca/course/  topics, worksheets, projects  
https://stat545.com/index.html  online book  
https://www.youtube.com/channel/UCrB-uourf2vxGeBnGjQrA0w  

SET-UP  
01_github: Setup      
02_basics: R, RStudio  

VERSION CONTROL and R MARKDOWN  
03_githubmd: Git, GitHub, RStudio     
04_rmd: R Markdown   
05_data-base: Data frames  

## STAT 545 Data wrangling, exploration and analysis with R  

https://stat545.stat.ubc.ca course at UBC

https://happygitwithr.com/ Git & GitHub  

## Old STAT 545 2015 on gitbooks
https://daattali.gitbooks.io/stat545-ubc-github-io/content/index.html   2015 book form  
https://daattali.gitbooks.io/stat545-ubc-github-io/content/topics.html  2015 book topics + class meetings  
https://daattali.gitbooks.io/stat545-ubc-github-io/content/syllabus.html 2015 class meetings  
https://daattali.gitbooks.io/stat545-ubc-github-io/content/bit006_github-browsability-wins.html  about git  

## Archive of old STAT 545 2015  
https://github.com/STAT545-UBC/STAT545-UBC-original-website  newer   
https://github.com/tonydurst/STAT545-UBC.github.io/tree/master  has git 

Jenny Bryan repo  
https://github.com/rstudio-education/stat545/tree/master

GitHub Student repo  
https://github.com/daattali/UBC-STAT545/tree/master  

## Intro to STAT 545  
https://speakerdeck.com/jennybc/ubc-stat545-2015-cm001-intro-to-course 

## Topic list
https://daattali.gitbooks.io/stat545-ubc-github-io/content/topics.html  2015

* [Install R and Rstudio](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block000_r-rstudio-install.html)  
* [Setup Git GitHub RStudio](https://daattali.gitbooks.io/stat545-ubc-github-io/content/git00_index.html)  
* [Intro to R and RStudio, scripts, workspace, working directory, RStudio Project](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block002_hello-r-workspace-wd-project.html)  
* [Dataframes: care and feeding of data in R](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block006_care-feeding-data.html)  
* [R objects (beyond data.frames) and indexing](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block004_basic-r-objects.html)  
* [Test drive R Markdown](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block007_first-use-rmarkdown.html)  
* [Data visualization with ggplot2, quantitative and categorical variables, colors, multiple plots](https://daattali.gitbooks.io/stat545-ubc-github-io/content/graph00_index.html)  
* [dplyr package for data manipulation](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block009_dplyr-intro.html)  
* [Writing R functions](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block011_write-your-own-function-01.html)  
* [plyr package for split-apply-combine](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block013_plyr-ddply.html)  
* [Factors](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block014_factors.html)  
* [Write and read files](https://github.com/STAT545-UBC/STAT545-UBC.github.io/blob/master/cm011_files-out-in-script.r)  
* [Tidy data](https://daattali.gitbooks.io/stat545-ubc-github-io/content/bit002_tidying-lotr-data.html)  
* [Regular expressions; character data](https://daattali.gitbooks.io/stat545-ubc-github-io/content/block022_regular-expression.html)  
* [Automate an analytical pipeline](https://daattali.gitbooks.io/stat545-ubc-github-io/content/topics.html#:~:text=All%20the%20automation%20things)  
* [Building R packages](https://daattali.gitbooks.io/stat545-ubc-github-io/content/packages00_index.html)  
* [Building Shiny apps: interactive pages, apps, graphics](https://daattali.gitbooks.io/stat545-ubc-github-io/content/packages00_index.html)  
* [Get data off the web: expose data, code, results on the web ]

* Generate reports from R scripts and R Markdown  
* Data aggregation; "apply: functions, `dplyr`  
* Coding style and project organization  
* Version control with Git; collaboration via GitHub  
* Distribute data and code via an R package  

## Syllabus: class meetings and homework  
https://daattali.gitbooks.io/stat545-ubc-github-io/content/syllabus.html  2015

STAT545A Exploratory Data Analysis   
[cm001](https://daattali.gitbooks.io/stat545-ubc-github-io/content/cm001_course-intro-sw-install-account-signup.html): Intro to course; S/W install; acct sign-ups  
[cm002](https://daattali.gitbooks.io/stat545-ubc-github-io/content/cm002_r-rstudio-intro.html): Deep Thoughts about data analytic work; intro to R and RStudio  
[cm003](https://daattali.gitbooks.io/stat545-ubc-github-io/content/cm003_r-objects-git-toe-dip.html): Git(Hub) and (R) Markdown crash course  
[cm004](https://daattali.gitbooks.io/stat545-ubc-github-io/content/cm004_care-feeding-data.html): Data.frames: care and feeding of data  
[cm005](https://daattali.gitbooks.io/stat545-ubc-github-io/content/cm005_ggplot2.html): Graphics: intro to ggplot2  
[cm006](https://daattali.gitbooks.io/stat545-ubc-github-io/content/cm006_rmarkdown.html0): R Markdown  
cm007: dplyr: single table verbs, Basic flavors of R objects  
cm008: dplyr: joins, Basic flavors of R objects  
cm009: Split-Apply-Combine, Writing your own R functions  
cm010: Split-Apply-Combine, Writing your own R functions  
cm011: Tidy data and reshaping  
cm012: Be the boss of your factors  
cm013: Effective graphs  
cm014: Practical graphing tips  

STAT547M Basic Training for Data Science  
cm101: Getting data out of R (and back in)  
cm102: Regular expressions and character data  
cm103: Data cleaning  
cm104: TBA  
cm105: Task automation and pipelines, GNU Make  
cm106: ditto  
cm107: Build your first R package  
cm108: ditto  
cm109: Build your first Shiny app  
cm110: ditto  
cm111: Get data from the web  
cm112: ditto  

[hw01](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw01_edit-README.html): Edit README.md  
[hw02](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw02_explore-gapminder-use-rmarkdown.html): Explore Gapminder and use R markdown  
[hw03](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw03_dplyr-and-more-ggplot2.html): Manipulate and summarize the Gapminder data with dplyr; make companion figs with ggplot2  
[hw04](http://stat545-ubc.github.io/hw04_write-function-use-plyr.html): Manipulate and summarize the Gapminder data with custom functions and plyr  
[hw05](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw05_factor-boss-files-out-in.html): Prove you are in control of factors by writing and reading files  
[hw06](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw06_repo-hygiene-figure-boss.html): Optional, clean your course repo  
[hw07](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw07_data-wrangling-grand-finale.html): Data wrangling Grand Finale  
[hw08](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw08_data-cleaning.html): re: handling character data and data cleaning  
[hw09](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw09_automation.html): Automating Data-analysis Pipelines  
[hw10](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw10_package.html): Write an R package  
[hw11](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw11_build-shiny-app): Build a Shiny app  
[hw12](https://daattali.gitbooks.io/stat545-ubc-github-io/content/hw12_data-from-web): Get data from the web  

## Original website   
https://github.com/STAT545-UBC/STAT545-UBC-original-website  newer   
https://github.com/tonydurst/STAT545-UBC.github.io/tree/master  has git   

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

Jennifer (Jenny) Bryan:  I teach and perform lots of data analysis. 
BA in econ and german, PhD biostatistics, assoc prof @ UBS  
50% statistics / 50% Michael Smith Laboratories  
Software Engineer at Posit on the tidyverse/r-lib team

Class culture  

* teach you to fish (learn from documentation, learning examples, google, stackoverflow)  
* reward engagement, intellectual generosity and curiosity (speak up, share success OR failure, show interest)  
* zero tolerance of plagiarism (generate your own approach, write some code, describe the process). Process is more important than product.  

Goal: work with a data set you choose. Think about datasets you'd like to prepare and analyze.

## Selected links from slides  
https://github.com/tonydurst/STAT545-UBC.github.io/blob/master/cm001_course-intro-sw-install-account-signup.md  

  * [The Big Data Brain Drain: Why Science is in Trouble](http://jakevdp.github.io/blog/2013/10/26/big-data-brain-drain/)
  * [The data science Venn diagram](http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram)
  * [Slides from Hadley Wickham's talk in the Simply Statistics Unconference](http://t.co/D931Og8mq3)
  * 2014-08-17 NYT article [For Big-Data Scientists:, 'Janitor Work' Is Key Hurdle to Insights](http://www.nytimes.com/2014/08/18/technology/for-big-data-scientists-hurdle-to-insights-is-janitor-work.html?partner=rss&emc=rss&smid=tw-nytimesscience&_r=0) by Steve Lohr
  * [Data carpentry](http://mimno.infosci.cornell.edu/b/articles/carpentry/) (response to NYT article re: janitor work)
  * [The Forgotten Job of a Data Scientist: Editing](http://www.john-foreman.com/blog/the-forgotten-job-of-a-data-scientist-editing)
  * [10 things statistics taught us about big data analysis](http://simplystatistics.org/2014/05/22/10-things-statistics-taught-us-about-big-data-analysis/)
  * [The 80/20 rule of statistical methods development](http://simplystatistics.org/2014/03/20/the-8020-rule-of-statistical-methods-development/)
  * [Don't use Hadoop - your data isn't that big](http://www.chrisstucchio.com/blog/2013/hadoop_hatred.html)
  * [Most data isn’t "big," and businesses are wasting money pretending it is](http://qz.com/81661/most-data-isnt-big-and-businesses-are-wasting-money-pretending-it-is/)
  * [Big data is like teenage sex](https://www.facebook.com/dan.ariely/posts/904383595868)
  * [Edward Tufte](http://www.edwardtufte.com) book [chapter 5 on the Challenger Disaster](http://www.edwardtufte.com/tufte/books_textb)
  * "Let's Practice What We Preach: Turning Tables into Graphs". The American Statistician, Volume 56, Number 2, 1 May 2002, pp. 121-130(10) by Gelman A, Pasarica C, Dodhia. [via JSTOR](http://www.jstor.org/stable/3087382)
  * [Data Sharing and Management Snafu in 3 Short Acts](https://www.youtube.com/watch?v=N2zK3sAtr-4&feature=youtu.be), a video
  * [The R Project](http://www.r-project.org)
  * [RStudio IDE](http://www.rstudio.com/products/rstudio/)
  * [R Markdown](http://rmarkdown.rstudio.com)
  * [knitr](http://yihui.name/knitr/)
  * ["FINAL".doc](http://www.phdcomics.com/comics/archive.php?comicid=1531) from PHDCOMICS
  * [Git](http://git-scm.com)
  * [GitHub](https://github.com)
  * [The Best Map Ever Made of America’s Racial Segregation](http://www.wired.com/design/2013/08/how-segregated-is-your-city-this-eye-opening-map-shows-you/?viewall=true)
    - [The Racial Dot Map](http://www.coopercenter.org/demographics/Racial-Dot-Map)
    - [unorthodox123/RacialDotMap](https://github.com/unorthodox123/RacialDotMap) on GitHub
  * [Foodborne Chicago finds dodgy restaurants with tweets, and R](http://blog.revolutionanalytics.com/2013/08/foodborne-chicago.html)
    - [corynissen/foodborne_classifier](https://github.com/corynissen/foodborne_classifier) on GitHub
  * [Roger Peng](http://www.biostat.jhsph.edu/~rpeng/)
  * [GNU Make for Reproducible Data Analysis](http://zmjones.com/make/)
  * [stackoverflow](http://stackoverflow.com)

