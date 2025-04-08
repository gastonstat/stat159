# STAT 159 - Reproducible and Collaborative Statistical Data Science

- __Descrtipion__: This course teaches "the why and how" of reproducible and collaborative research by combining questions of good computational practice in science, open science and statistical data analysis, in the context of today's research environment. We will interleave practical topics in software engineering and statistical computing with broader discussions on elements of the philosophy of science and the foundations of statistics.

- __Details__: We will rely on R and RStudio ecosystems, but the core ideas presented here can be equally implemented with tools in Python, Julia, or any other programming language.

- __Instructor__: [Gaston Sanchez](https://www.gastonsanchez.com)

- __Lecture__: 3 hours of lecture per week

- __Assignments__: around 6 HW assignments

- __Exams__: one midterm exam, and final project

- __Textbook__:
    + Statistics, 4th edition by Freedman, Pisani, and Purves (FPP)

- __Prerequisites__: Statistics 133, 134, 135


-----


## Software

We are going to be using several tools along this course. Which means that you will have to install the following programs (_if you run into any installation problems google it first or check youtube videos; if that doesn't work then ask the GSI or the instructor_):

- __Git__ (version control)
	- [Downloads](https://git-scm.com/downloads)

- __GitHub__
	- You will also need to open an account on [GitHub](https://github.com/) (unless you already have one): [https://github.com/join](https://github.com/join)

- __R__ (statistical & data analysis software)
	- [Mac OS X](https://cran.r-project.org/bin/macosx/)
	- [Windows](https://cran.r-project.org/bin/windows/base/)
	- [Linux](https://cran.r-project.org/bin/linux/)

- __RStudio__ (IDE for R)
	- [Downloads](https://www.rstudio.com/products/rstudio/download/)

- __Rtools__ (tools for building R in Windows)
	- If you work with Windows, you will need to download Rtools
	- [Download](https://cran.r-project.org/bin/windows/Rtools/)

- __Tex/LaTeX__ (typesetting system)
	- [MacTeX](https://tug.org/mactex/) (Mac OS X)
	- [MikTeX](http://miktex.org/download) (Windows)

- __pandoc__ (universal document converter)
	- [Installing](http://pandoc.org/installing.html)

- __Xcode__ (IDE for Mac OS X)
	- If you work on a Mac, you will need to install Xcode
	- [Mac OS X](https://developer.apple.com/xcode/downloads/)


-----


## 1. Introduction

:card_index: __ABOUT__:

We begin with the usual review of the course policies, logistics, overall expectations, topics in a nutshell, etc.

Every Data Analysis Project goes through a cycle: At the conceptual level, we'll identify the main stages of the data analysis cycle using sports data _Long Jump world records_ which are one of the oldest standing records in athletics.

<br>

:book: __READING__: 

- Slides

<br>

:pencil2: __TOPICS__:

+ __Introduction__
    - The Data Analysis Cycle (DAC)
    - First contact with R and RStudio

+ __How not to do a Data Analysis__
    - Understand limitations of WYSIWYG tools
    - Advantages of using WYSIWYM tools


-----


## 2. Reproducibility Crisis

:card_index: __ABOUT__:

In this module we review an infamous case of irreproducibility: the _Reinhart-Rogoff Debacle_

<br>

:book: __READING__: 

Reinhart and Rogoff Reading Materials

- [Researchers Finally Replicated Reinhart-Rogoff, and There Are Serious Problems.](http://rooseveltinstitute.org/researchers-finally-replicated-reinhart-rogoff-and-there-are-serious-problems/) (by Mike Konczal)

- [Reinhart, Rogoff... and Herndon: The student who caught out the profs](http://www.bbc.com/news/magazine-22223190) (by Ruth Alexander)

- [The Reinhart and Rogoff Controversy: A Summing Up](http://www.newyorker.com/news/john-cassidy/the-reinhart-and-rogoff-controversy-a-summing-up) (by John Cassidy) 

- [FAQ: Reinhart, Rogoff, and the Excel Error That Changed History](http://www.bloomberg.com/news/articles/2013-04-18/faq-reinhart-rogoff-and-the-excel-error-that-changed-history)

- [Holy Coding Error Batman](http://krugman.blogs.nytimes.com/2013/04/16/holy-coding-error-batman/) (by Paul Krugman)

- [Reinhart and Rogoff working paper "Growth in a Time of Debt"](http://www.nber.org/papers/w15639)

- [Various links for the "Special: Reinhart & Rogoff Debacle"](http://morelivers.blogspot.fr/2013/04/21st-apr-special-reinhart-rogoff-debacle.html) (curated by Moreliver's)

<br>

:pencil2: __TOPICS__:

+ __RR Case Study__
    - Who are Reinhart and Rogoff (R&R)?
    - What is their affiliation?
    - About their working paper "Growth in times of debt" (GTD)
    	+ What is the main thesis of the paper?
    	+ What are their main findings?
    	+ What are their conclusions?
    - Story behind R&R fiasco:
    	+ After the publication of GTD, who tries to reproduce their work?
    	+ What is the story of the irreproducibility attempt?
    	+ What is the cause of the irreproducibility?


-----


## 3. Introduction to Markdown

:card_index: __ABOUT__:

Markdown is a lightweight markup language, originally created by 
[John Gruber](http://daringfireball.net/) and Aaron Swartz allowing people 
"to write using an easy-to-read, easy-to-write plain text format, then convert 
it to structurally valid XHTML (or HTML)". 

- About markup languages
- Why do we need to use a markup language (and a text editor)?
- What is the issue with word processors?

Dynamic Documents with R

- What is a dynamic document?
- Dynamic documents and markup languages
- Dynamic documents require a parser and renderer
- In R, we have the packages "knitr", "rmarkdown", and "shiny"
- Before knitr we had "Sweave" (with LaTeX)
- LaTeX is still the _de rigueur_ scientific typesetting system

<br>

:book: __READING__: 

- Slides

<br>

:pencil2: __TOPICS__:

+ __Markdown__
    - More [technical details about Markdown](http://daringfireball.net/projects/markdown/)
    - Markdown [philosophy](https://daringfireball.net/projects/markdown/syntax#philosophy)
    - Small demos:
    	+ from markdown to html
    	+ from markdown to latex
    	+ from markdown to pdf
    	+ from markdown to docx
    	+ etc
    - Work with markdown online editors
    - Let's check some basics with [markdown live preview](http://markdownlivepreview.com/) 
    - .Rmd files in R

+ __R Markdown__
    - Working with so-called "Dynamic Documents"
    - Weaving and Knitting
    - Combining narrative and code


-----


## 4. File-System and Path Names

:card_index: __ABOUT__:

In any Data Analysis Project (DAP), you'll be working with files:

- data, code, images, docs, etc
- some files are inputs, some files are outputs
- a project is a NETWORK of relationships between files
- although you don't see it, there is a network (connections among files)
- FUNDAMENTAL to know where files are, and manage their pathnames

<br>

:book: __READING__: 

- Slides

<br>

:pencil2: __TOPICS__:

+ __DAPs, Files and Directories__
    - A data analysis project involves working with files
    - Classification of files (inputs, instructions, outputs)
    - How does a data analysis project looks like from the files standpoint?
    - Understanding the structure of directories and files
    - Understanding the network of relationships between files
    - It is fundamental to know where files are, and manage their pathnames
    - It is important to set up a good file structure
    - How to NOT organize things
    - What kinds of things can change in a project?
    - A data analysis project may experience a variety of changes
    - A data analysis project can be viewed as an iterative pipeline
    - Ultimate goal: being prepared to recreate the analysis when anything changes


-----


## 5. Command Line Interface (CLI)

:card_index: __ABOUT__:

In the preceding module you learned that any Data Analysis Project (DAP) involves working with files. Since all DAPs involve working with files, we need to discuss/recap the concept of filesystem and path names. We also need to discuss how to interact with your computer using a Command Line Interface (CLI).

- Using a GUI (Graphical User Interface)
- Using a CLI (Command Line Interface)
- Advantages and disadvantages of GUIs
- Advantages and disadvantages of CLIs

<br>

:book: __READING__: 

- Slides

<br>

:pencil2: __TOPICS__:

+ __Navigating the file system__
    - Understand the tree structure
    - Pathnames: absolute and relative
    - The Root directory `/`
    - The working directory
    - The home directory
    - Special directories: 
    	+ home `/~`
    	+ current `.`
    	+ parent `..`
    - Absolute names
    - Relative names
    - Descending the tree
    - Ascending the tree

+ __Some basic bash commands__
    - `ls`
    - `pwd`
    - `cd`
    - `mkdir`
    - `touch`
    - `rm`
    - `rmdir`
    - `cp`
    - `mv`


-----


## 6. Version Control with Git (part 1)

:card_index: __ABOUT__:

In this week, we begin the first part for learning about Git, a Version Control System (VCS)

<br>

:book: __READING__: 

- Slides

<br>

:pencil2: __TOPICS__:

+ __Git Basics__
    - Git configuration
    - Creating a new remote repository
    - Status
    - Adding changes
    - Committing changes
    - Log

+ __Github and Remote Repositories__
    - Create a Remote Repositories
    - Adding a remote repo to a local repo
    - Pushing changes to a remote repository
    - Cloning repos
    - Forking repos


-----


## 7. More and Github (part 2)

:card_index: __ABOUT__:

In this week, we continue with the second part about Git.

<br>

:book: __READING__: 

- Slides

<br>

:pencil2: __TOPICS__:

+ __More Git__
    - Remote Repositories
    - Github
 

-----


## 8. Basics of Makefiles

:card_index: __ABOUT__:

In this week, we introduce Make which is a software for automating processes.

<br>

:book: __READING__: 

- Slides

<br>

:pencil2: __TOPICS__:

+ __Automation with Make__
    - About GNU Make
    - Scripts to automate things: we won't really use Make for compiling, but for automating tasks
    - The main advantage is its capability to track timestamps
    - It only executes things that have changed
    - I've found that the learning curve is a bit steep


-----


## 9. Writing Functions and Sharing Code

:card_index: __ABOUT__:

Often, you will need to encapsulate some of your code and create functions.

<br>

:book: __READING__: 

- <a href="http://www.nature.com/news/2010/101013/full/467753a.html" target="_blank"><i class="fa fa-newspaper-o" aria-hidden="true"></i> Publish your computing code: it is good enough</a> (by Nick Barnes)

- <a href="http://www.nature.com/news/2003/030623/full/news030623-6.html" target="_blank"><i class="fa fa-newspaper-o" aria-hidden="true"></i> Openness makes software better sooner</a> (by Philip Ball)

- <a href="http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=6200247" target="_blank"><i class="fa fa-newspaper-o" aria-hidden="true"></i> Code Sharing is Associated with Research Impact in Image Processing</a> (by Patrick Vandewalle)


<br>

:pencil2: __TOPICS__:

- __Advatanges of writing functions__
	+ Avoid DRY
	+ Enable Reusability
	+ Facilitate Extensibility
	+ Force you to better think
- __How to write functions?__
	+ start small
	+ make sure your code works
	+ don't worry initially about optimization
	+ encapsulate your code
	+ think about the users
	+ think about special cases
- __Good practices for writing functions__
	+ Modularize
	+ Prefer simple functions
	+ Choose a naming style (descriptive)
	+ Be consistent
	+ Argument names
	+ Length (lines of code)
- __Profiling__
	+ Efficiency
	+ Debugging
 

-----


## 10. Testing Functions

:card_index: __ABOUT__:

Often, you will need to encapsulate some of your code and create functions.

<br>

:book: __READING__: 

- [Advanced R - Functions](http://adv-r.had.co.nz/Functions.html) by Hadley Wickham.

- [testthat: Get Started with Testing](https://journal.r-project.org/archive/2011-1/RJournal_2011-1_Wickham.pdf) by Hadley Wickham.

- [Example of unit testing R code with testthat](http://www.johndcook.com/blog/2013/06/12/example-of-unit-testing-r-code-with-testthat/) by John D. Cook.

- [Code and Data for the Social Sciences: A Practitioner's Guide](https://web.stanford.edu/~gentzkow/research/CodeAndData.pdf) by Matthew Gentzkow and Jesse Shapiro.


<br>

:pencil2: __TOPICS__:

- __Testing functions__
	+ Write basic test
	+ Does it do what is expected to do?
	+ Does it fail as expected?
	+ What about extreme cases?
	+ What about nonsensical inputs?
	+ Writing tests


-----


## 11. Testing Functions

:card_index: __ABOUT__:

Often, you will need to encapsulate some of your code and create functions.

<br>

:book: __READING__: 

- [Advanced R - Functions](http://adv-r.had.co.nz/Functions.html) by Hadley Wickham.

- [testthat: Get Started with Testing](https://journal.r-project.org/archive/2011-1/RJournal_2011-1_Wickham.pdf) by Hadley Wickham.

- [Example of unit testing R code with testthat](http://www.johndcook.com/blog/2013/06/12/example-of-unit-testing-r-code-with-testthat/) by John D. Cook.

- [Code and Data for the Social Sciences: A Practitioner's Guide](https://web.stanford.edu/~gentzkow/research/CodeAndData.pdf) by Matthew Gentzkow and Jesse Shapiro.


<br>

:pencil2: __TOPICS__:

- __Testing functions__
	+ Write basic test
	+ Does it do what is expected to do?
	+ Does it fail as expected?
	+ What about extreme cases?
	+ What about nonsensical inputs?
	+ Writing tests


-----


## 12. Sharing Code and Licenses

:card_index: __ABOUT__:

This week we consider the licensing aspects for papers, figures, and media files. We also consider the licensing aspects for code and software. Likewise, you'll learn how to choose between different licenses described by the Open Source Initiative.Choosing a license for your work: 1) media, and 2) code.

<br>

:book: __READING__: 

- Victoria Stodden's paper, and focus on section III: _Copyright and the Sharing of Scientific Work_.

- <a href="http://web.stanford.edu/~vcs/papers/ijclp-STODDEN-2009.pdf" target="_blank"><i class="fa fa-newspaper-o" aria-hidden="true"></i> Enabling Reproducible Research: Licensing Scientific Innovation</a> (by Victoria Stodden)

- <a href="https://opensource.org/licenses" target="_blank"><i class="fa fa-newspaper-o" aria-hidden="true"></i> Licenses and Standards</a> (by Open Source Initiative)

<br>

:pencil2: __TOPICS__:

- __Licenses__
    - Why is the US copyright law a barrier to the sharing of scientific work?
    - Why Scientific Research has no natural legal home?
    - What is the conflict between copyright law and reproducible research?
    - Do licenses remove or rescind copyright protection?
    - What do licenses are good for?
    - What is a principle for scientific licensing?
    - Briefly discuss the different frameworks of licenes:
    	+ for paper, figures, and other media files
    	+ for code (source, and compiled)
    	+ what about data?
    - What are Creative Common Licenses?
    - Explain various conditions:
    	+ Attribution (CC BY)
    	+ Share Alike
    	+ Non-Commercial
    	+ No Derivative works
    - Describe the different types of Creative Common Licenses for media:
    	+ Attribution
    	+ Attribution - No Derivative Works
    	+ Attribution - Non-Commercial - No Derivative Works
    	+ Attribution - Non-Commercial
    	+ Attribution - Non-Commercial - Share Alike
    	+ Attribution - Share Alike
    - What is the duration of a CC license?
    - What is the Creative Commons CC0 protocol?
    - What is the Reproducible Research Standard (RRS) proposed by Stodden?


-----


## 13. Sharing Data Sets

:card_index: __ABOUT__:

This week we discuss guideline for sharing data sets.

<br>

:book: __READING__: 

- <a href="http://ojs.library.queensu.ca/index.php/IEE/article/view/4608" target="_blank"><i class="fa fa-newspaper-o" aria-hidden="true"></i> Nine simple ways to make it easier to (re)use your data</a> (by White et al, 2013)

- <a href="https://github.com/jtleek/datasharing" target="_blank"><i class="fa fa-newspaper-o" aria-hidden="true"></i> How to share data with a statistician</a> (by The Leek group guide to data sharing)

- <a href="http://kbroman.org/dataorg/" target="_blank"><i class="fa fa-newspaper-o" aria-hidden="true"></i> Organizing data in spreadsheets</a> (by Karl Broman)

<br>

:pencil2: __TOPICS__:

- __Data Sharing Considerations__
	1. Share your data
	2. Provide metadata
	3. Provide an unprocessed form of the data
	4. Use standard data formats
	5. Use good null values
	6. Make it easy to combine your data with other datasets
	7. Perform basic quality control
	8. Use an established repository
	9. Use an established and open license

- __Publishing Data__
    - _When publishing data make an explicit and robust statement of your wishes_.
    How do we do this?
    - _Use a recognized waiver or license that is appropriate for data._
    What license(s) can we use?
    - What is the recommended license if you have data that is publicly funded?

- __How to share data with a statistician__
	1. The raw data
	2. The tidy dataset
	3. The code book
	4. How to code variables
	5. The instruction list/script

- __Data Organization in Spreadsheets__
	1. Be consistent
	2. Writing dates
	3. Fill in all of the cells
	4. Put just one thing in a cell
	5. Make it a rectangle
	6. Create a data dictionary
	7. No calculations in the raw data files
	8. Don't use font color or highlighting as data
	9. Choose good names for things
	10. Make backups
	11. Use data validation to avoid data entry mistakes
	12. Save the data in plain text files
	13. Other things to avoid

