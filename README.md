
<!-- README.md is generated from README.Rmd. Please edit that file -->

# transfersh

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![R build
status](https://github.com/kvasilopoulos/transfersh/workflows/R-CMD-check/badge.svg)](https://github.com/kvasilopoulos/transfersh/actions)
[![CRAN
status](https://www.r-pkg.org/badges/version/transfersh)](https://CRAN.R-project.org/package=transfersh)
<!-- badges: end -->

The goal of {transfersh} is to utilize the power of
[transfer.sh](https://transfer.sh) through R.  is a website and not a
script, which helps users to share files from the command-line an
efficient way. It won’t required any additional software to work except
pre-installed application such as curl.

## Install

You can install the development version from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("kvasilopoulos/transfer")
```

## Example

This is a basic example which shows you how to use {transfersh}:

``` r
library(transfersh)
```

To upload a file you can easily use the name of the file and the path
where the file is located, if it is not in the working directory. In
case of a folder or multiple files `tf_upload` will bundle all contents
and zip it into a single file. Then it will upload the zip and delete
the zip that was created locally.

## File

``` r
tf_upload("file.txt", path = "inst/examples")
#>  --- Uploaded: transfer.sh --- 
#> https://transfer.sh/D7r28/file.txt
```

## Folder

``` r
tf_upload("folder", path = "inst/examples")
#>  --- Uploaded: transfer.sh --- 
#> https://transfer.sh/rGobn/transferxa1966d.zip
```
