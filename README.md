pa_2: averages of duration, f0, and intensity
================
Hunter Metz
2024-03-18

``` r
# load packages

library(tidyverse)
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ## ✔ ggplot2   3.4.4     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.3     ✔ tidyr     1.3.1
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

``` r
library(readr)

# read and print csv file into Rstudio

data <- read_csv("data/data.csv")
```

    ## Rows: 10 Columns: 4
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (1): info
    ## dbl (3): durationV, f0, int
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
print(data)
```

    ## # A tibble: 10 × 4
    ##    info    durationV    f0   int
    ##    <chr>       <dbl> <dbl> <dbl>
    ##  1 capo_1       0.12 108.   48.0
    ##  2 capo_2       0.23 102.   58.5
    ##  3 pinto_1      0.17 102.   63.1
    ##  4 pinto_2      0.19  85.1  53.8
    ##  5 pujo_1       0.12 112.   66.7
    ##  6 pujo_2       0.14  88.0  57.1
    ##  7 quemo_1      0.15 113.   68.8
    ##  8 quemo_2      0.1   95.2  59.8
    ##  9 testo_1      0.18  99.8  63.4
    ## 10 testo_2      0.14  94.4  56.7

``` r
# Calculation of average of duration
avg_duration <- mean(data$durationV, na.rm = TRUE)

# Calculation of average of f0
avg_f0 <- mean(data$f0, na.rm = TRUE)

# Calculation of average of intensity
avg_intensity <- mean(data$int, na.rm = TRUE)

# Print the averages
cat("Average duration:", avg_duration, "\n")
```

    ## Average duration: 0.154

``` r
cat("Average f0:", avg_f0, "\n")
```

    ## Average f0: 99.992

``` r
cat("Average intensity:", avg_intensity, "\n")
```

    ## Average intensity: 59.591

``` r
#Averages all together: average duration was 0.154, average f0 was 99.992, and the average intensity was 59.591
```
