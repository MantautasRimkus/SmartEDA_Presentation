STAT600 - Automated EDA in R
================

After getting some new dataset, doing a proper exploratory data analysis
(EDA) is very important part. This help to better understand the
structure of our data, potential problems and project the steps needed
to use the particular data set for modelling.

Most of the data analysts would agree that data preparation (cleaning,
putting to the correct format) and exploration of a data set takes big
chunk of the time devoted to the project.

(Un)Fortunately people are lazy, thus some started developing some ways
how to spead up the EDA part.

Here I present 4 R libraries that has some functions for automatic EDA -
`DataExplorer`, `Hmisc`, `dlookr`, `explore`.

``` r
library("DataExplorer")
library("Hmisc")
library("dlookr")
library("exploreR")
```

For each of the package, the data used comes from suggestions of
packages itself.

\#\#DataExplorer

This package is created by Boxuan Cui. Here are showed three functions
from DataExplorer package - `introduce()`, `plot_intro()`, and
`create_report()`. The datasets used for a presentation - airquality and
diamonds.

``` r
DataExplorer::introduce(airquality)
```

    ##   rows columns discrete_columns continuous_columns all_missing_columns
    ## 1  153       6                0                  6                   0
    ##   total_missing_values complete_rows total_observations memory_usage
    ## 1                   44           111                918         6376

``` r
DataExplorer::plot_intro(airquality)
```

![](Generator_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

``` r
DataExplorer::create_report(diamonds, y="price", output_file="DataExplorer_diamonds_report.html")
```

If you interested in more packages and their comparison, there are some
references: - The Landscape of R Packages for Automated Exploratory Data
Analysis by Mateusz Staniak and Przemysław Biecek -
<https://github.com/mstaniak/autoEDA-resources>
