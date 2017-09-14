# Gapminder!
Kaitlyn Harper  
September 14, 2017  



Hello! We're going to explore the Gapminder dataset today! First, we need to load the dataset from Rstudio. Note: for this markdown, you'll see my code in gold and the output in blue! 

<style>
div.color pre { background-color:lightskyblue; }
div.color pre.r { background-color:gold; }
</style>

<div class = "color">

```r
# Load tidyverse + all corresponding packages!
library(tidyverse)
```

```
## Loading tidyverse: ggplot2
## Loading tidyverse: tibble
## Loading tidyverse: tidyr
## Loading tidyverse: readr
## Loading tidyverse: purrr
## Loading tidyverse: dplyr
```

```
## Conflicts with tidy packages ----------------------------------------------
```

```
## filter(): dplyr, stats
## lag():    dplyr, stats
```

```r
# Load gapminder dataset
library(gapminder)
data("gapminder")

# View the first 6 lines of the data set (to make sure it's there)
head(gapminder)
```

```
## # A tibble: 6 x 6
##       country continent  year lifeExp      pop gdpPercap
##        <fctr>    <fctr> <int>   <dbl>    <int>     <dbl>
## 1 Afghanistan      Asia  1952  28.801  8425333  779.4453
## 2 Afghanistan      Asia  1957  30.332  9240934  820.8530
## 3 Afghanistan      Asia  1962  31.997 10267083  853.1007
## 4 Afghanistan      Asia  1967  34.020 11537966  836.1971
## 5 Afghanistan      Asia  1972  36.088 13079460  739.9811
## 6 Afghanistan      Asia  1977  38.438 14880372  786.1134
```

```r
# This is also a great way to look at the head of this data set! 
glimpse(gapminder)
```

```
## Observations: 1,704
## Variables: 6
## $ country   <fctr> Afghanistan, Afghanistan, Afghanistan, Afghanistan,...
## $ continent <fctr> Asia, Asia, Asia, Asia, Asia, Asia, Asia, Asia, Asi...
## $ year      <int> 1952, 1957, 1962, 1967, 1972, 1977, 1982, 1987, 1992...
## $ lifeExp   <dbl> 28.801, 30.332, 31.997, 34.020, 36.088, 38.438, 39.8...
## $ pop       <int> 8425333, 9240934, 10267083, 11537966, 13079460, 1488...
## $ gdpPercap <dbl> 779.4453, 820.8530, 853.1007, 836.1971, 739.9811, 78...
```
</div>
Sweet! So it looks like we have a few different types of variables in our data set. The country and continent variables are **factors**; the year and pop variables are **integers**; the lifeExp and gdpPercap variables are **numerics**.

Okie doke. Let's take a look at some of the variables now. For example, if we want to find out how many unique countries are in this data set, we could do this:
<div class = "color">

```r
# Unique number of countries
length(unique(gapminder$country))
```

```
## [1] 142
```
</div>
Looks like there are 142 countries in our data set. Interesting. I wonder if all the continents are present.. Let's look! 
<div class = "color">

```r
unique(gapminder$continent)
```

```
## [1] Asia     Europe   Africa   Americas Oceania 
## Levels: Africa Americas Asia Europe Oceania
```
</div>
Huh, looks like North and South America are lumped into one, and Antarctica is missing. 

I'm pretty sure we're going to get to plotting in the next hw assignment, so let's just explore some of the simple stats for this data set. 







