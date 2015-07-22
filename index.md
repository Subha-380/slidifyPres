---
title       : First Presentation
subtitle    : slidify
author      : Sk
job         :
framework   : revealjs       # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : default      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Different Plots in R

---
* R provides many ways to Visualise our data for analysis. Here are a few:




####  Base Plot

```r
data(cars)
with(cars,plot(speed,dist))
```

![plot of chunk unnamed-chunk-2](figure/unnamed-chunk-2-1.png) 

---
####  Lattice Plot

```r
library(lattice)
state <-data.frame(state.x77,region=state.region)
xyplot(Life.Exp ~Income|region,data=state,layout = c(4,1))
```

![plot of chunk unnamed-chunk-3](figure/unnamed-chunk-3-1.png) 

---
####  ggplot2 system       

```r
library(ggplot2)
data(diamonds)
diamonds<-diamonds[sample(1:nrow(diamonds),2000),]
ggplot(diamonds, aes(carat, price))+geom_point(color="firebrick")
```

![plot of chunk unnamed-chunk-4](figure/unnamed-chunk-4-1.png) 

---

#### Histogram

```r
hist(faithful[,2], breaks = 15, col = 'skyblue', border = 'white',xlab = "Waiting time between eruptions", main = "Histogram")
```

![plot of chunk unnamed-chunk-5](figure/unnamed-chunk-5-1.png) 
---



