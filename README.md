# STAT 159 - Reproducible and Collaborative Statistical Data Science

- __Descrtipion__: This course teaches "the why and how" of reproducible and collaborative research by combining questions of good computational practice in science, open science and statistical data analysis, in the context of today's research environment. We will interleave practical topics in software engineering and statistical computing with broader discussions on elements of reproducible data analysis.

- __Details__: We will rely on R and RStudio ecosystems, but the core ideas presented here can be equally implemented with tools in Python, Julia, or any other programming language.

- __Instructor__: [Gaston Sanchez](https://www.gastonsanchez.com)

- __Lecture__: 3 hours of lecture per week

- __Assignments__: around 6 HW assignments

- __Exams__: typically one midterm exam, and final project

- __Prerequisites__: Statistics 133, 134, 135

- __Policies__:
    + [Lab](https://github.com/gastonstat/course-policies/blob/main/policy-lab.md)
    + [HW](https://github.com/gastonstat/course-policies/blob/main/policy-hw.md)
    + [Email](https://github.com/gastonstat/course-policies/blob/main/policy-email.md)
    + [Academic Integrity](https://github.com/gastonstat/course-policies/blob/main/policy-academic-integrity.md)


-----


## Software

We are going to be using several tools along this course. Which means that you will have to install the following programs (_if you run into any installation problems google it first or check youtube videos; if that doesn't work then ask the GSI or the instructor_):

- __Git__ (version control)
	- https://git-scm.com/downloads

- __GitHub__ (Git repository hosting service)
	- https://github.com/
  - Open account (if you don't have one): https://github.com/join

- __R__ (statistical & data analysis software)
	- Mac OS X: https://cran.r-project.org/bin/macosx/
	- Windows: https://cran.r-project.org/bin/windows/base/
	- Linux: https://cran.r-project.org/bin/linux/

- __Posit RStudio__ (IDE for R)
	- Desktop (free) version: https://posit.co/downloads/

- __Rtools__ (tools for building R in Windows)
	- If you work with Windows, you will need to download Rtools
	- https://cran.r-project.org/bin/windows/Rtools/

- __Tex/LaTeX__ (typesetting system)
	- MacTeX (Mac OS X): https://tug.org/mactex/
	- MikTeX (Windows): http://miktex.org/download

- __pandoc__ (universal document converter)
	- https://pandoc.org/installing.html

- __Xcode__ (IDE for Mac OS X)
	- If you work on a Mac, you may need to install Xcode
	- Mac OS X: https://developer.apple.com/xcode/downloads/


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
