# Tutorial to discuss reproducible research using `markdown`, `knitr` and version control using git & github

As we discussed and demonstrated in class on thursday, there are two major pieces to this.

1. Version Control
2. Making your research reproducible.

## Version Control.

Since we already discussed the basics of version control, I will not go over it again in too much detail. There is a nice, gentle introduction  at [software carpentry](http://software-carpentry.org/v5/novice/git/index.html) that I recommend you go through.

Basically it allows you to keep track of all of the "versions" of your scripts (or any other text files). Simply by *committing* your changes to your scripts using version control, all of the changes you made (and when you made them) are kept track of. You can 'undo' changes in the scripts as well. It is also extremely useful if you are working collaboratively on scripts (or on manusscripts).

We will be using [`git`](http://git-scm.com/) as our version control system (Another popular one that you can use in Rstudio is *subversion* or *svn*). There are many tutorials out there to introduce git (including the software carpentry one above). I think [github does a good job to get started](https://help.github.com/). 

There is also a number of cheatsheets for the commands. I happen to use [this one alot](https://training.github.com/kit/downloads/github-git-cheat-sheet.pdf).

## Making your research more reproducible

While you can just as easily just provide your scripts (i.e. `MyAnalysis.R`) along with your data in a data repository like [DRYAD](http://datadryad.org/), it is often much clearer to provide some clarity to your analysis. Essentially provide sufficient information to explain what you are doing. Indeed it is possible (and not that difficult) to generate a single text document that contains all of the information to generate both your analysis, including figures, generate a markup document (like LaTeX) which generates a PDF of your manuscript. This same file can be parsed to generate just the analysis script (i.e. just the `.R` bits). In class the `.tex` and `.R` files as well as  PDFs that I generate are a result of this where I have generated a combined text file with prose and script (in a `.Rnw` file), and I use `Sweave()` to generate the `.tex` file and `tangle()` to generate the `.R` file. The .tex file can be compiled into making a PDF (.tex is the extension for the tex and LaTeX language).

However learning LaTeX has a bit of a learning curve. So instead we will focus on using a very simple syntax highlighting system called "markdown" that can easily be integrated with **R** using the library `knitr`. When you combine **R** functions with markdown it is often called "R markdown" and files with this have the extension `.Rmd` (as opposed to just `.md` for markdown).

First make sure to install the `knitr` library. 
```{r install_packages}
install.packages("knitr")
```


