# data_skeleton

A skeletal file hierarchy for setting up data analysis projects.

Clone this repo when you're getting ready to deal with a new set of data. This is inspired by approaches like [ProjectTemplate](http://projecttemplate.net/getting_started.html), but is more appropriate for my own analyses. It might not be exactly what you need, but it might be a place to start.

The project root directory contains the following folders:

* data

   This folder contains "raw" data files used for the analysis.

* process

   This folder contains scripts that process raw data. In my analyses, I usually create a database that contains raw and processed data. The scripts that load this data into the database lives here. Each file name should begin with a number indicating the order in which it was created and run so that somebody else (e.g., future you) can reproduce the database and analysis.

* R

   When using R for analysis, source files that define useful functions should go here. You might want to make a `python` folder or something like that.

* report

   This contains scripts or files (e.g., [R Markdown](http://rmarkdown.rstudio.com/) files) to produce reports. Each report should encompass a single "analysis" of the data.

* export

   It would be nice if collaborators (and other interested people) meant what they said when they asked for "raw data". This directory contains scripts that dump data for sharing.

# How to use this

Clone this repository and set up a new one (replace `yourproject` with the name of the a folder for your project):

```
git clone https://github.com/eamoncaddigan/data_skeleton.git yourproject
cd yourproject
rm -rf .git/
git init
git add .
```
