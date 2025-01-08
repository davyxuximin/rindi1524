
<!-- README.md is generated from README.Rmd. Please edit that file -->

# rindi1524

<!-- badges: start -->

<!-- badges: end -->

The goal of rindi1524 is to split string.

## Installation

You can install the development version of rindi1524 from
[GitHub](https://github.com/) with:

``` r
# install.packages("pak")
pak::pak("davyxuximin/rindi1524")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(rindi1524)
(x <- "alfa,bravo,charlie,delta")
#> [1] "alfa,bravo,charlie,delta"
strsplit(x, split = ",")
#> [[1]]
#> [1] "alfa"    "bravo"   "charlie" "delta"
stringr::str_split(x, pattern = ",")
#> [[1]]
#> [1] "alfa"    "bravo"   "charlie" "delta"
```

``` r

str_split_one(x, pattern = ",")
#> [1] "alfa"    "bravo"   "charlie" "delta"
```

Use `str_split_one()` when the input is known to be a single string. For
safety, it will error if its input has length greater than one.

`str_split_one()` is built on `stringr::str_split()`, so you can use its
`n` argument and stringr’s general interface for describing the
`pattern` to be matched.

``` r
str_split_one(x, pattern = ",", n = 2)
#> [1] "alfa"                "bravo,charlie,delta"

y <- "192.168.0.1"
str_split_one(y, pattern = stringr::fixed("."))
#> [1] "192" "168" "0"   "1"
```
