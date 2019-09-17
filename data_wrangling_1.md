Data Wrangling 1
================
Sarah McLarnan
2019-09-17

Load in a dataset
-----------------

``` r
litters_data = read_csv(file = "./data/FAS_litters.csv")
```

    ## Parsed with column specification:
    ## cols(
    ##   Group = col_character(),
    ##   `Litter Number` = col_character(),
    ##   `GD0 weight` = col_double(),
    ##   `GD18 weight` = col_double(),
    ##   `GD of Birth` = col_double(),
    ##   `Pups born alive` = col_double(),
    ##   `Pups dead @ birth` = col_double(),
    ##   `Pups survive` = col_double()
    ## )

``` r
litters_data = janitor::clean_names(litters_data)

fas_pups = read_csv(file = "./data/FAS_pups.csv")
```

    ## Parsed with column specification:
    ## cols(
    ##   `Litter Number` = col_character(),
    ##   Sex = col_double(),
    ##   `PD ears` = col_double(),
    ##   `PD eyes` = col_double(),
    ##   `PD pivot` = col_double(),
    ##   `PD walk` = col_double()
    ## )

``` r
fas_pups = janitor::clean_names(fas_pups)
```

Read in an excel file
---------------------

``` r
library(readxl)
mlb11_data = read_excel(
  path = "./data/mlb11.xlsx",
  range = "A1:D7")
```

Read in a SAS file
------------------

``` r
library(haven)
pulse_data = read_sas("./data/public_pulse_data.sas7bdat")
```
