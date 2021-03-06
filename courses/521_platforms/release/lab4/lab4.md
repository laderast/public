Lab 4 - RStudio projects and driving Git from RStudio
================

In Lab 4, you will reinforce your understanding of good file naming and project organisation habits, as well as learn how to create and use R Studio Projects, and get practice with driving Git from RStudio.

Submission Instructions
-----------------------

rubric={mechanics:2}

-   [Follow the general lab instructions](https://ubc-mds.github.io/resources_pages/general_lab_instructions/)

1.0. File naming best practices
-------------------------------

Reflect on the "[Let's talk about filenames and Data Science project organization](https://github.ubc.ca/MDS-2018-19/DSCI_521_platforms-dsci_students/blob/master/lectures/lecture6/lecture6.Rmd)" lecture to answer the questions below.

### Question 1.0.0.

rubric={correctness:1}

What are the three principles for file names that we discussed in lecture?

> YOUR ANSWER GOES HERE

### Question 1.0.1.

rubric={reasoning:2}

For each of the three priciples above, explain (in your own words) why we should follow them.

> YOUR ANSWER GOES HERE

### Question 1.0.2.

rubric={reasoning:2}

What date format do we recommend you use for everything, especially filenames? Why is that date format useful/helpful for data science? Provide an example date in that format.

> YOUR ANSWER GOES HERE

2.0. Project organisation
-------------------------

One very userful learning strategy for Data Science is to look and reflect on how others in the field "do" things, and then incorporate the "good" and "useful" ideas/strategies/tools into your own practice. In this next question we will try to learn more about how to organise data science projects. We will look at both "data analysis" projects, where the focus is answering a research/business question using data science tools, as well as data science tool projects, where the focus is creating a tool you or others can later use to help solve a research/business question with data analysis.

### Question 2.0.0. - Identify public repositories in hosted version control for data analysis projects and data science tools

rubric={reasoning:8,writing:2}

-   Search or browse hosted version control (*e.g.,* Github and/or Bitbucket) and identify 3 public repositories for data analysis projects and three public repositories for data science tools. You can choose from the list of repositories below, **or** you can find others **you are interested in**:

-   Data analysis project Github repositories:
    -   [Pleistocene-aged stone artefacts from Jerimalai, East Timor: Long term conservatism in early modern human technology in island Southeast Asia](https://github.com/benmarwick/Pleistocene-aged-stone-artefacts-from-Jerimalai--East-Timor) by Ben Marwick *et al.*
    -   [WorldBank GDP data sets and evaluation](https://github.com/bici-sancta/gdp_worldbank) by Bici Sancta
    -   [High temporal and spatial diversity in marine RNA viruses implies that they have an important role in mortality and structuring plankton communities](https://github.com/jooolia/RdRp_454_amplicons_Jericho_and_SOG) by Julia Gustavsen *et al.*
    -   [The Horse Transcriptome project](https://github.com/drtamermansour/horse_trans) by Tamer Mansour
    -   [Historical horse population in Canada](https://github.com/ttimbers/equine_numbers_value_canada) by Tiffany Timbers
-   Data science tool Github repositories:
    -   [`geoparser`](https://github.com/ropenscilabs/geoparser)
    -   [`screed`](https://github.com/dib-lab/screed)
    -   [`AutoQC`](https://github.com/BillMills/AutoQC)
    -   [`rpanama`](https://github.com/dgrtwo/rpanama)
    -   [`southafricastats`](https://github.com/juliasilge/southafricastats)
    -   [`dplyr`](https://github.com/hadley/dplyr)
    -   [`pandas`](https://github.com/pydata/pandas)
    -   [`packrat`](https://github.com/rstudio/packrat)
    -   [`conda`](https://github.com/conda/conda)
    -   [`virtualenv`](https://github.com/pypa/virtualenv)
    -   [Docker](https://github.com/docker/docker)
-   As proof of your search and research, identify these repositories with their URLs and write a brief summary paragraph to describe each project (this can be very high level).

-   In about half (1/2) to three quarters (3/4) of a page, reflect on the following:
-   How are data **analysis project repositories** generally organized? What is the folder structure and what content is included in these folders
-   How are data science **tool repositories** generally organized? What is the folder structure and content is included in these folders?
-   What similarities do you observe between data analysis project and data science tool repositories?
-   What differences do you observe between data analysis project and data science tool repositories?

3.0. Creating RStudio projects
------------------------------

In R focused projects, it is often helpful to make the project an "RStudio project" (see docs on how to do this [here](https://support.rstudio.com/hc/en-us/articles/200526207-Using-Projects)). When you do this, you create another file in your project's root directory - an `*.Rproj` file. This "special" file is helpful, and can provide you the following features:

-   double clicking on the `*.Rproj` file opens a new R Session with RStudio with the working directory set to the directory containing the `*.Rproj` file
-   allows you to use Git through RStudio
-   allows you to specify what to save (or not save) in regards to your R workspace and R history
-   helps you to manage your R packages with `packrat` (more on this in workflows)

### Question 3.0.0.

rubric={mechanics:2}

1.  Make this homework repository an RStudio project with Git version control. Put the `*.Rproj` file under version control using RStudio's Git interface and push it to GitHub.

2.  Set the project options as recommended in the [Workflow: projects chapter in R for Data Science](http://r4ds.had.co.nz/workflow-projects.html). Take screenshots of the "R General" and the "Git/SVN" tabs of the Project Options window to prove you did this. *note - you can get to the the Project Options window via Tools &gt; Project Options (once you have created or opened an RStudio project*

> YOUR SCREENSHOTS GO HERE.

4.0. Knitting/rendering to a directory other than the project root
------------------------------------------------------------------

### Question 4.0.0.

rubric={mechanics:8}

Last lab when you created R Markdown documents, you left them in the project root. This made for a less than organised project. Let's use what we learned in lecture to knit/render a document that lives in the `doc` directory. In this example we will have the `.Rmd` file live in `doc` and have the rendered `.md` file be written there as well. We will also practice bringing in some other files (either data or images) that live somewhere other an `doc` (for data, let's put it in a directory called `data`, for images let's put it in a directory called `img`).

For example, the directory structure after the question below might look like this:

    project_root/
    ├── doc/
    │   ├── file_files
    │   ├── file.Rmd
    │   ├── file.md
    ├── img/
    │   ├── an_image.png
    ├── data/
    │   ├── some_data.csv
    ├── lab4_files
    ├── lab4.Rmd
    ├── lab4.md

Specific instructions are laid out below.

1.  create a `doc` directory in this lab's repo
2.  create a new R Markdown file in the `doc` directory. That `.Rmd` should have at least 2 text sections and 2 code chunks. It should also load an image that you put in a directory called `img` and/or use R to load some data that you put in a directory called `data`.
3.  add this line to your setup code chunk: `knitr::opts_knit$set(root.dir = here::here())` (note - you will need to install the `here` package)
4.  knit/render the `.Rmd` by either typing `rmarkdown::render("doc/hist_horse_pop.Rmd")` in the console or by clicking Knit Directory &gt; Project Directory.
5.  Put all the files associated with this `.Rmd` under version control using RStudio's Git interface and push the files to GitHub.

### (Optional) Question 4.0.1.

rubric={mechanics:1}

Ever think you might want to write and publish an online book? Or a manual? Well thanks again to Yihui Xie (developer of knitr and Xaringan!) you can do this with the tools you learned in this class using the [`bookdown` R package](https://bookdown.org/yihui/bookdown/).

You have already seen some Bookdown books in this program. For example, [R for Data Science](http://r4ds.had.co.nz/) and [Happy Git and GitHub for the useR](http://happygitwithr.com/) were both created with Bookdown.

For this optional question, following the instructions in the [Getting Started](https://bookdown.org/yihui/bookdown/get-started.html) chapter of the `bookdown` book to build your own book using the template. Then edit the template and make a small, simple demo book that is your own. What to put in it? Of course something Data Sciency could work, but for this lab you might not have time, so some easyish ideas are:

-   photos
-   recipes
-   jokes

Paste you link to your published book below:

> YOUR LINK TO YOUR BOOK GOES HERE
