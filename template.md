Simple document
================
Fang Wang
2024-9-10

I’m an R Markdown document!

# Section 1

Here’s a **code chunk** that samples from a *normal distribution*:

``` r
## eval = FALSE: code will be displayed but not executed; results are not included.
## echo = FALSE: code will be executed but not displayed; results are included.
## include = FALSE: code won’t be executed or displayed.
## message = FALSE and warning = FALSE: prevents messages and warnings from being displayed.
## results = hide and fig.show = hide: prevents results and figures from being shown, respectively.
## collapse = TRUE: output will be collapsed into a single block at shown at the end of the chunk.
## error: errors in code will stop rendering when FALSE; errors in code will be printed in the doc when TRUE. The default is FALSE and you should almost never change it. 
samp = rnorm(100)
length(samp)
```

    ## [1] 100

# Section 2

I can take the mean of the sample, too! The mean is -0.0205672.

# Section 3: learning assessement

This is code for the learning assessment at P8105.

I loaded necessary package “tidyverse”

``` r
la_df =
  tibble(
    norm_samp = rnorm(n=500, mean=1),
    samp_g0 = norm_samp >1,
    abs_v_samp = abs(norm_samp)
  )

ggplot(la_df, aes(x=abs_v_samp))+
         geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](template_files/figure-gfm/learning%20assessment-1.png)<!-- -->

Here is code to create a histogram.

``` r
ggplot(la_df, aes(x=abs_v_samp))+
         geom_histogram()
```

# Section 4: Formating text

*italic* or *italic* **bold** or **bold** `code` superscript<sup>2</sup>
and subscript<sub>2</sub>

## Headings

# 1st Level Header

## 2nd Level Header

### 3rd Level Header

## Lists

- Bulleted list item 1

- Item 2

  - Item 2a

  - Item 2b

1.  Numbered list item 1

2.  Item 2. The numbers are incremented automatically in the output.

## Tables

| First Header | Second Header |
|--------------|---------------|
| Content Cell | Content Cell  |
| Content Cell | Content Cell  |
