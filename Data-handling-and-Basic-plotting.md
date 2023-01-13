---
output: 
  html_document: 
    keep_md: yes
    toc: yes
    theme: readable
    highlight: pygments
    fig_caption: yes
---


*R for Statistics and Data Visualization - An Introduction for Life Scientists 1*

# Data handling and Basic plotting

###### Elizabeth Oladapo


<br/>

In this section, we will focus on loading data into R and saving files into your project directory and sub directories, exploring data and basic plotting of graphs. 

<br/>

### 1. Download the datasets

Download the datasets we will be using in this training: 

[ElephantsMF.csv](http://rcg.group.shef.ac.uk/courses/R/Dataset/ElephantsMF.csv) 

[IRIS.csv](http://rcg.group.shef.ac.uk/courses/R/Dataset/IRIS.csv)

Move the two .csv files into the data folder in your project folder ("R-training") on your local machine

<br/>

### 2. Importing data from the data folder into R

Any .csv file can be imported into R using the function read_csv() and assigning it to a new variable to store the result.
<br/>

Prior to loading your data, make sure to load the required libraries for this section and set up you script with appropriate annotations

__Something to note__: Always annotate your code (with # and break into sections with # and ------) so that when you look back on what you have coded. You understand in detail what a line, chunk or even section of code is trying to accomplish.


```r
### Data Management and Basic graphing (* you can create a section or chapter by putting "----" @ the end of this line)
### Elizabeth Oladapo
### 13 February 2023

# Analyzing the data on 288 African elephants that lived through droughts in the first two years of life.
# The data contains 3 variables and 288 observations.
# The variables are; Age, Height and sex

##Source:
# Data are from Phyllis Lee, Stirling University, and are related to Lee, P., et al. (2013), "Enduring consequences of early 
# experiences: 40-year effects on survival and success among African elephants," Biology Letters, 9: 
# 20130011.



# Load the packages I need with the function library()

library("tidyverse")
```

```
## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
## ✔ ggplot2 3.4.0      ✔ purrr   1.0.0 
## ✔ tibble  3.1.8      ✔ dplyr   1.0.10
## ✔ tidyr   1.2.1      ✔ stringr 1.5.0 
## ✔ readr   2.1.3      ✔ forcats 0.5.2 
## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
## ✖ dplyr::filter() masks stats::filter()
## ✖ dplyr::lag()    masks stats::lag()
```



A check can be performed with  the function file.exists() which will print TRUE if the file is present in the working directory.


```r
file.exists("data/ElephantsMF.csv")
```

```
## [1] TRUE
```

Now that the file exists in the working directory, we will need to import it into R to start making R work hard on it.

Import the ElephantsMF.csv file and assign it to a variable name called "Elephants_data"


```r
# Loading the required data

Elephants_data <- read_csv("data/ElephantsMF.csv")
```

```
## Rows: 288 Columns: 3
## ── Column specification ────────────────────────────────────────────────────────
## Delimiter: ","
## chr (1): Sex
## dbl (2): Age, Height
## 
## ℹ Use `spec()` to retrieve the full column specification for this data.
## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
```

Look at the data using the function glimpse(), to be sure you have loaded the correct data

```r
# Looking at the data

glimpse(Elephants_data) # or Elephants_data or str(Elephants_data)
```

```
## Rows: 288
## Columns: 3
## $ Age    <dbl> 1.40, 17.50, 12.75, 11.17, 12.67, 12.67, 12.25, 12.17, 28.17, 1…
## $ Height <dbl> 120.00, 227.00, 235.00, 210.00, 220.00, 189.00, 225.00, 204.00,…
## $ Sex    <chr> "M", "M", "M", "M", "M", "M", "M", "M", "M", "M", "M", "M", "M"…
```

```
Question
There are three variables in the Elephants_data, which of them are the explanatory variables and which is a response variable?

```

<br/>

### 3. Visualizing the data

Visualize the data by generating your first plot in R using the function ggplot() from the package, ggplot2.


```r
## Visualize the data1

ggplot(Elephants_data, aes(x = Age, y=Height))+
  geom_point()    # a continuous response variable with a continuous explanatory variable producing scatterplot
```

![](Data-handling-and-Basic-plotting_files/figure-html/unnamed-chunk-5-1.png)<!-- -->

```r
## Visualize the data2

ggplot(Elephants_data, aes(x = Sex, y=Height))+
  geom_col()    # a continuous response variable with a binary explanatory variable producing barcharts
```

![](Data-handling-and-Basic-plotting_files/figure-html/unnamed-chunk-6-1.png)<!-- -->
<br/>

### 4. Visualizing the data



<br/>

__Exercise 1__

The output you should get, and the graph
that should be produced, are provided below.

You should:
• select the fruit and grazing columns
• filter fruit that is > 90 OR < 30
• assign this subset of the data to the object fg90_30
• look at the data
• produce a scatterplot of Fruit (y) versus Grazing (x), proving that there are only values >90 or <30


<br/>
### 6. Save your first script!







Growth from conception to reproductive onset in African elephants (Loxodonta africana) provides insights into phenotypic plasticity, individual adaptive plastic responses and facultative maternal investment. Using growth for 867 and life histories for 2652 elephants over 40 years, we demonstrate that maternal inexperience plus drought in early life result in reduced growth rates for sons and higher mortality for both sexes. Slow growth during early lactation was associated with smaller adult size, later age at first reproduction, reduced lifetime survival and consequently limited reproductive output. These enduring effects of trading slow early growth against immediate survival were apparent over the very long term; delayed downstream consequences were unexpected for a species with a maximum longevity of 70+ years and unpredictable environmental experiences.








<br/>

__Congratulations on your first script in R, we are now ready for the next stage__

__Return__ to the main course page:
https://github.com/Lizzydapsy/R-for-Data-Analysis and click on "Manipulating Data and advanced Plotting".