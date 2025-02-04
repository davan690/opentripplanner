
<!-- README.md is generated from README.Rmd. Please edit that file -->

# OpenTripPlanner for R <a href='https://itsleeds.github.io/'><img src='man/figures/logo.png' align="right" height=180/></a>

[![Travis build
status](https://travis-ci.org/ropensci/opentripplanner.svg)](https://travis-ci.org/ropensci/opentripplanner)
[![codecov](https://codecov.io/gh/ropensci/opentripplanner/branch/master/graph/badge.svg)](https://codecov.io/gh/ropensci/opentripplanner)
[![AppVeyor Build
Status](https://ci.appveyor.com/api/projects/status/github/ropensci/opentripplanner?branch=master&svg=true)](https://ci.appveyor.com/project/mem48/opentripplanner)
[![Project Status: Active – The project has reached a stable, usable
state and is being actively
developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![](https://badges.ropensci.org/295_status.svg)](https://github.com/ropensci/onboarding/issues/295)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3558311.svg)](https://doi.org/10.5281/zenodo.3558311)

The goal of OpenTripPlanner for R is to provide a simple R interface to
[OpenTripPlanner (OTP)](https://www.opentripplanner.org/). The OTP is a
multimodal trip planning service written in Java. For more information
on what OTP is, see the [prerequisites
vignette](https://docs.ropensci.org/opentripplanner/articles/prerequisites.html).

This package can be used to interface with a remote instance of OTP
(e.g. a website) or help you set up and manage a local version of OTP
for private use. Basic setup and routing functions are outlined in the
[getting started
vignette](https://docs.ropensci.org/opentripplanner/articles/opentripplanner.html),
while advanced functionality such as batch routing, isochrones, and
customised setup is described in the [advanced features
vignette](https://docs.ropensci.org/opentripplanner/articles/advanced_features.html).

## Installation

### OpenTripPlanner

To use OpenTripPlanner on your local computer you will need to install
Java 8 and download the latest version of OTP. Instructions on
installing Java and setting up OTP can be found in the [prerequisites
vignette](https://docs.ropensci.org/opentripplanner/articles/prerequisites.html).

### R Package

Install the package using the **devtools** package as follows:

``` r
# If you do not already have the devtools package
install.packages("devtools")
# Install the package from GitHub
devtools::install_github("ropensci/opentripplanner")
# Load the package
library(opentripplanner)
```

## Usage

The package contains three groups of functions:

Functions for setting up a local instance of OTP:

1.  `otp_dl_jar()` To download the OTP Jar file;
2.  `otp_dl_demo()` To download the demo data for the Isle of Wight;
3.  `otp_build_graph()` To make a OTP graph from raw data;
4.  `otp_setup()` To start up a local instance of OTP;
5.  `otp_make_config()` To make a config object;
6.  `otp_validate_config()` To validate a config object;
7.  `otp_write_config()` To save a config object as a json file.

Functions for connecting to a local or remote instance of OTP:

1.  `otp_connect()` To connect to OTP.

Functions for retrieving data from OTP:

1.  `otp_plan()` To get routes from A to B;
2.  `otp_isochrone()` To get isochrone maps;
3.  `otp_geocode()` To get the locations of named places e.g. road
    names.

Results are returned as [sf
objects](https://CRAN.R-project.org/package=sf).

## Tests

As this package does not work without a working connection to OTP, tests
only run on machines that have the environment variable `I_have_OTP`
with the value `TRUE`. You can add this with
`usethis::edit_r_environ()`.

``` r
Sys.getenv("I_have_OTP")
```

## Acknowledgement

This package was built off the [tutorial by Marcus
Young](https://github.com/marcusyoung/otp-tutorial).

## Contribution

Please note that the `opentripplanner` project is released with a
[Contributor Code of Conduct](CODE_OF_CONDUCT.md). By contributing to
this project, you agree to abide by its terms. Bug reports and comments
are welcome as Github
[Issues](https://github.com/ropensci/opentripplanner/issues) and code
submissions as [Pull
Requests](https://github.com/ropensci/opentripplanner/pulls).

## Package Status

This package is part of ongoing research at the University of Leeds. A
stable version of the package (v0.2.0) is
[available](https://github.com/ropensci/opentripplanner/releases/tag/0.2).
We intend to bring a verson to CRAN soon.

[![ropensci\_footer](https://ropensci.org/public_images/ropensci_footer.png)](https://ropensci.org)
