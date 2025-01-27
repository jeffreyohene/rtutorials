
<!-- README.md is generated from README.Rmd. Please edit that file -->

# rtutorials

<!-- badges: start -->

[![R-CMD-check](https://github.com/statistik-lehre/rtutorials/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/statistik-lehre/rtutorials/actions/workflows/R-CMD-check.yaml)
<!-- badges: end -->

*This R package is currently under active development.*

Acquire basic statistics and R knowledge (somewhat) interactively and
self paced.

- **Language**: German

- **Audience**: Written for statistic newbies, in our case 3rd semester
  bachelor students of environmental and civil engineering

### Quick Start / Installation

By installing this package, you add handcrafted lessons to your RStudio
Tutorials Pane.

**Prerequisites**: R + RStudio installed

Copy the following code into your RStudio [console
pane](https://cengel.github.io/R-intro/backgroud.html#rstudio-console-and-command-prompt)
and hit Enter.

``` r
install.packages(c("devtools", "learnr"))
devtools::install_github("statistik-lehre/rtutorials")
```

**Error**: If R reports an error like

    Error in
    utils::download.file(url, path, method = method, quiet = quiet, :
    Herunterladen von
    ‘<https://api.github.com/repos/statistik-lehre/rtutorials/tarball/HEAD>’
    fehlgeschlagen

this could be due to the large size of the package in relation to your
download speed. `install_github()` has a default timeout of 60 seconds.
Set a longer timeout with the command below and retry the installation.

``` r
options(timeout = 9999999)
devtools::install_github("statistik-lehre/rtutorials")
```

**Error**: Another error, although more uncommon looks like this:

    Timeout was reached: [api.github.com] Resolving timed out after 10000 milliseconds

Solution: Try to connect to the internet. If you are connected, wait a
few minutes and try again. Likely, this error occurs because you hit the
download rate limit of the GitHub API, e.g. installed too many large
packages from GitHub in a short period of time.

## Contents

All tutorials are in German. Here are the titles translated to English
for the convenience of the English readers. A German detailed overview
can be found at the end.

Note that tutorials are being written and published step by step, the
list below includes planned tutorials as well. Look at `inst/tutorials`
in the main branch, it is the most up to date way of finding out what is
published at the moment.

| Block | Tutorial Subject                      | Tutorial name        |
|-------|---------------------------------------|----------------------|
| 1     | **Introduction**                      | `1a_intro`           |
| 1     | **Exploring Functions and Arguments** | `1b_funktionen`      |
| 1     | **Scientific Process**                | `1c_prozess`         |
| 2     | **Vectors**                           | `2a_vektoren`        |
| 2     | **Indexing**                          | `2b_indizierung`     |
| 2     | **Data Frames**                       | `2c_dataframes`      |
| 3     | **Data Import**                       | `3a_import`          |
| 3     | **Scales and Factors**                | `3b_skalen`          |
| 3     | **Measures of Central Tendency**      | `3c_zentraletendenz` |
| 4     | Measures of Spread                    |                      |
| 4     | Visualization Basics                  |                      |
| 4     | Visualization with ggplot2            |                      |
| 5     | Sampling                              |                      |
| 5     | t-Tests                               |                      |
| 5     | Levene-Test                           |                      |
| 6     | Chi Squared                           |                      |
| 6     | Power Analysis                        |                      |
| 6     | Correlations                          |                      |
| 7     | Simple Linear Regression              |                      |
| 7     | Scientific Process Long               |                      |
| 7     | Programming Basics                    |                      |

## Accessing the tutorials

**The graphical way**

In RStudio, you will see a tutorials tab in the top right. Click it to
select from different tutorials and start them. You will see all
tutorials of all different packages, including example tutorials from
the `learnr` package.

It might require an RStudio restart until the tutorials of the
`rtutorials` package appear.

Click “Start Tutorial” to learn interactively. That’s it!

Below is some code which achieves the same thing without a navigating a
click- and scrollable menu surface.

**The command way**

To list all available tutorials from `rtutorials`:

``` r
learnr::available_tutorials(package = "rtutorials")
#> Available tutorials:
#> * rtutorials
#>   - 1a_intro           : "Einführung"
#>   - 1b_funktionen      : "Funktionen erkunden"
#>   - 1c_prozess         : "Wissenschaftlicher Prozess"
#>   - 2a_vektoren        : "Vektoren"
#>   - 2b_indizierung     : "Indizierung bei Vektoren"
#>   - 2c_dataframes      : "Arbeit mit Tabellen"
#>   - 3a_import          : "Datenimport"
#>   - 3b_skalen          : "Skalenniveaus"
#>   - 3c_zentraletendenz : "Maße der zentralen Tendenz"
#>   - template           : "template"
```

And to run the individual tutorials, run:

``` r
learnr::run_tutorial("name", package = "rtutorials")
```

For example:

``` r
learnr::run_tutorial("1a_intro", package = "rtutorials")
```

## Contributing

Feedback and contributions are welcome!

If you spot a typo, some incorrect content or see just a better way to
do it, you are welcome to collaborate. Either report it as an issue or
even better, fix it yourself!

Fork the repo, contribute and please submit your changes with a pull
request.

The tutorial source code is found at `inst/tutorials/…/….Rmd`.

A **template tutorial** for the stylings we use is found at
`inst/tutorials/template`, but not included in the built package.

For more in depth guidelines on `learnr` tutorials, check out the
[`learnr`](https://rstudio.github.io/learnr/) documentation.

Also, we try to maintain a set of `good first issues` that helps you get
started with contributing to this project.

## License

We would be happy to hear from you if you want to modify or redistribute
the contents of this course.

This software comes to you with an OpenSource license, because we are
fond believers in the strength of commons.

However, the use is restricted to noncommercial purposes and only
applies to the contents of this repository. Other course materials that
you may get as one of our students are subject to copyright.

## Authorship

The tutorials are written by Lukas Bruelheide, Gesa Graf and Marie
Klosterkamp, who is also leading the project.

## Funding

Kassel University, HessenHub, 2022 - 2023
