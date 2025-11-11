# Marker identification analysis workshop

## Overview

This workshop will focus on performing marker identification analysis of transcriptomic data and visualising the results. We will identify markers on single-cell RNA-seq data using methods in the `smartid` package to explore feature importance in class and individual samples. Following this, we will perform gene-set scoring using tools from the `smartid` package. Overall, we will demonstrate a TF-IDF-based approach to process the data, identify the markers, visualise and interpret resutls using `smartid` package.

The workshop will be organised into two broad sections:
* Calculate score for each feature in each sample
* Scale and transform scores in regard of class
* Identify markers for each class based on GMM

Detailed material can be found [here](https://gene233.github.io/MarkerIdentificationWorkflow/articles/workshop_smartid.html).

## Pre-requisites 

The course is aimed at PhD students, Master's students, and third & fourth year undergraduate students. 
Some basic R knowledge is assumed - this is not an introduction to R course. 
If you are not familiar with the R statistical programming language it is compulsory that you work through an introductory R course before you attend this workshop.

## _R_ packages used

The following key R packages will be used: 

* `smartid`
* `mclust`
* `mastR`

## Time outline

| Activity                                                        | Time |
|-----------------------------------------------------------------|------|
| Introduction & setup                                            | 15m  |
| Part 1. Calculate score for each feature in each sample         | 20m  |
| Part 2. Scale and transform scores in regard of class           | 20m  |
| Part 3. Identify markers for each class based on GMM            | 20m  |
| Q & A                                                           | 15m  |


## Workshop goals and objectives

### Learning goals

 - Learn how to perform marker identification on scRNA-seq data in R.
 - Understand the challenges caused by rare population within scRNA-seq data.
 - Understand the importance of marker findings.

### Learning objectives

 - Perform a marker identification analysis and interpret the results.
 - Apply smartid to identify highly-specific markers for rare populations and to validate the results using scoring method in `smartid`.

## Workshop package installation 

### Guide

This is necessary in order to reproduce the code shown in the workshop. 
The workshop is designed for R `4.5` and can be installed using one of the two ways below.

### Via Docker image

If you're familiar with [Docker](https://docs.docker.com/get-docker/) you could use the Docker image which has all the software pre-configured to the correct versions.

```
docker run -e PASSWORD=password -p 8787:8787 gene233/markeridentificationworkflow:latest
```

Once running, navigate to <http://localhost:8787/> and then login with
`Username:rstudio` and `Password:password`.

You should see the Rmarkdown file with all the workshop code which you can run.

### Via GitHub

Alternatively, you could install the workshop using the commands below in R `4.5`.

```
install.packages('remotes')

# Install workshop package
remotes::install_github("Gene233/MarkerIdentificationWorkflow", build_vignettes = TRUE)

# To view vignettes
library(MarkerIdentificationWorkflow)
browseVignettes("MarkerIdentificationWorkflow")
```
