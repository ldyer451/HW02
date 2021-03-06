HW02\_B\_Graph-Mimic
================
Lucas Dyer

``` r
library("ggplot2")
library("magrittr") #so I can do some piping
data("diamonds")
data("mpg")
data("iris")
theme_set(theme_bw()) #I'll give you this one, you can set the theme individually for graphs
#or you can set the theme for all the graphs using theme_set()
#theme_bw() is best theme (IMO)

#for graph 3:
library("ggrepel")
```

## HW02 Part B

My submission for this part\! I welcome any feedback\!

### Graph 1

``` r
data("diamonds")
#hint think about the *position* the bars are in...
```

Using the diamonds dataset, make this graph:
![](HW02_B_Mimic_starter_files/figure-gfm/graph1%20code-1.png)<!-- -->

### Graph 2

``` r
data("iris")
```

Using the iris dataset, make this graph:

    ## `geom_smooth()` using formula 'y ~ x'

![](HW02_B_Mimic_starter_files/figure-gfm/graph%202%20code-1.png)<!-- -->

### Graph 3

You’ll need the information in this first box to create the graph

``` r
data("mpg")
corvette <- mpg[mpg$model == "corvette",]
#install
require("ggrepel") #useful for making text annotations better, hint hint
set.seed(42)
```

Now using the mpg dataset and the corvette dataset, make this graph:

![](HW02_B_Mimic_starter_files/figure-gfm/graoh%203%20code-1.png)<!-- -->

There is a trick to getting the model and year to print off together.
`paste()` is a useful function for this, also pasting together parts of
file names and parts of urls together.

### Graph 4

``` r
data(mpg)

#hint for the coloring, colorbrewer and you can set palette colors and make your graphs colorblind friendly
library(RColorBrewer)
display.brewer.all(colorblindFriendly = T) #take a look at the colorblindfriendly options
```

![](HW02_B_Mimic_starter_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

The above graph lets you see some colobrlind friendly palettes. For the
graph below, I used Set2.

Now using the above mpg dataset, make this graph

    ## `stat_bindot()` using `bins = 30`. Pick better value with `binwidth`.

![](HW02_B_Mimic_starter_files/figure-gfm/graph%204%20code-1.png)<!-- -->
