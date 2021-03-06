431 Assignment 1
================
Thomas E. Love
Due **2017-09-15** at noon. Version: 2017-08-27

-   [General Instructions](#general-instructions)
-   [The Data](#the-data)
-   [Question 1](#question-1)
-   [Question 2](#question-2)
-   [Question 3](#question-3)
-   [Question 4](#question-4)
-   [Question 5](#question-5)
-   [Question 6](#question-6)
-   [Question 7](#question-7)
-   [Question 8](#question-8)
-   [Question 9](#question-9)
-   [Question 10](#question-10)
-   [Question 11](#question-11)
-   [Some Additional Guidance on Getting Started](#some-additional-guidance-on-getting-started)

General Instructions
====================

This assignment requires you to analyze some data, and prepare a report in the form of an HTML, Word or PDF file, using R Markdown. We have provided you with a very useful R Markdown document template for this assignment called `YOURNAME-hw1.Rmd` that you should use to complete the assignment. The `YOURNAME-hw1.Rmd` file is part of the [downloadable data and code materials](https://github.com/THOMASELOVE/431data). Just click on the green **Click or download** button and select Download ZIP to get all of the files you'll need, including the `YOURNAME-hw1.Rmd` template.

1.  Your final submission should include both your final Markdown file (renamed to replace YOURNAME with your name) and either a Word document (`YOURNAME-hw1.docx`), PDF (`YOURNAME-hw1.pdf`) or HTML (`YOURNAME-hw1.html`) document generated from your R Markdown file. Submit your files via canvas.case.edu as described in the [Course Syllabus](https://thomaselove.github.io/431syllabus/).

2.  Use complete English sentences in each question where you provide a response.

3.  This assignment will be considerably easier after Class 2, and we have every expectation that you will read ahead in the [Course Notes](https://thomaselove.github.io/431notes/) a bit to complete the assignment successfully.

4.  You are welcome to discuss Assignment 1 with Dr. Love, the teaching assistants or your colleagues, but your answer must be prepared by you alone.

With regard to assignments, we are interested solely in helping you. To maintain our sanity, we have two rules:

1.  In general, we **do not** provide answers to questions that we receive *in the last 18 hours* before an assignment is due. So don't leave this (or anything else) until the last day.
2.  Late work is inappropriate for graduate school. Turning in an assignment more than one hour after the deadline will result in a very poor grade on the assignment. Submission of timely, but partial work is better than no submission at all.

If an assignment is scheduled so that you cannot complete it in a timely fashion, it is your responsibility to inform Dr. Love via email so he can evaluate the situation *at least 48 hours in advance* of the deadline.

The Data
========

The setup for this assignment involves the following R code, which is already contained in the `YOURNAME-hw1.Rmd` file.

``` r
knitr::opts_chunk$set(comment=NA)
options(width = 70)

library(MASS); library(tidyverse)
## make sure these libraries are installed in R
```

The data come from the `faithful` data frame contained in the base installation of R, specifically, within the `datasets` package. These data describe the duration of an eruption for the Old Faithful geyser in Wyoming's Yellowstone National Park, as well as the waiting time until the next eruption.

The commands below place the `faithful` data frame in a tibble called `hw1`, then display the tibble. We encourage you to use this `hw1` tibble to develop your answers to Questions 1-10.

    hw1 <- tbl_df(faithful)
    hw1

Use the command `?faithful` to see some additional details about these data. The `hw1` tibble contains observations on two variables:

-   `eruptions` = eruption time in minutes
-   `waiting` = waiting time to next eruption, also in minutes

Question 1
==========

Plot a histogram or other summary plot which meaningfully describes the distribution of the waiting times. Be sure it is very clearly labeled.

Question 2
==========

What appears to be a typical waiting time? Compare the mean, median and 80% trimmed mean (mean of the middle 80% of the observed waiting times.)

Question 3
==========

What is the inter-quartile range, and how does it compare to the standard deviation?

Question 4
==========

Is the distribution multi-modal or unimodal? How do you know?

Question 5
==========

Is the distribution skewed (and if so, in which direction) or is it essentially symmetric? How do you know?

Question 6
==========

Are there any unusual (outlier) values in the distribution, and if so, what are they?

Question 7
==========

Would a model using the Normal distribution be an appropriate way to summarize the waiting time data? Why or why not?

Question 8
==========

Plot a scatterplot of the waiting times (y-axis) vs. the eruption durations (x-axis) and be sure your plot is very clearly labeled. Describe your general impression of the plot: what sort of relationship do you see?

Question 9
==========

What is the correlation of waiting time with eruption duration? How would you interpret this result?

Question 10
===========

Would a linear model be an appropriate thing to use in attempting to predict the waiting time given the most recent eruption duration, based on these data? Why or why not? Add a simple least squares regression line to the plot.

Question 11
===========

Investigate questions 8-10 again using the `geyser` data in the `MASS` package, and compare your results appropriately.

Use the command `?MASS::geyser` to see some additional details about these data, and to learn more about how they differ from the data in our original data set, and specify those differences in your response. The commands below will place the relevant data for these questions in the `hw1extra` tibble.

    hw1extra <- tbl_df(MASS::geyser)
    hw1extra

Some Additional Guidance on Getting Started
===========================================

1.  Get R and R Studio and all of the suggested R packages and data sets onto your computer, [following these installation instructions](https://github.com/THOMASELOVE/431/blob/master/software-installation-431.md).

2.  Place the `YOURNAME-hw1.Rmd` document in a new clean directory in your computer - you might call the directory something helpful like `431hw1`, for instance. Change the name of the file from `YOURNAME-hw1.Rmd` to include your actual name.

3.  Once everything is loaded, start R Studio, and immediately build a new Project by selecting File ... New Project. Select to build the new project in an existing directory, and navigate to the directory you created in step 2. When the project has been built, you should see `431hw1` (or whatever name you gave) in the upper right of your R Studio screen.

4.  Use the Files menu to select and open your newly renamed version of the YOURNAME-hw1.Rmd file.

5.  Edit the R Markdown file at the top to include your actual name instead of YOURNAME in the title and author fields in the prelude.

6.  Click on the little down arrow next to the word Knit at the top left of the screen and run the Markdown file to see if it generates a result. You can select HTML (which should always work) or Word (which should work if you have a registered copy of Microsoft Office) or PDF (which will work if you have a functioning LaTeX installation - if you don't, see [the end of the Working with Data in R materials](https://github.com/THOMASELOVE/431/blob/master/431_2017_working-with-data-in-R.md).) Take a look at the result and see if it looks like it's working. I suggest HTML or Word for this assignment.

7.  Return to R Studio and complete the assignment by editing the R Markdown file to include sentences in English and code chunks. Again, the [Working with Data in R](https://github.com/THOMASELOVE/431/blob/master/431_2017_working-with-data-in-R.md) document and, of course, the [Course Notes](https://thomaselove.github.io/431notes/) may help.

8.  Save your work, frequently, and re-knit it occasionally to see that changes you've made are working.

9.  Don't be afraid to ask questions, either of Professor Love, or of the teaching assistants, either in person, or by emailing **431-help at case dot edu**.
