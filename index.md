---
title       : Are you a Survivor ?
subtitle    : a statistical overview of the Titanic mishap
author      : Praveen Bysani 
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## About the Data

The package "datasets" contains the table "Titanic", that provides data about the survivors in the tragic incident of Titanic. The dataset has 4 dimensions

1. Class: The class in which the passenger is travelling
2. Sex: The gener of the passenger
3. Age: The age group of the passenger
4. Survived: Information about whether the passenger is survived or not

The table contains the frequency of passengers in all the possible combinations of above factors

---
## Overview of data


```r
TitanicData <- as.data.frame(Titanic)
summary(TitanicData)
```

```
##   Class       Sex        Age     Survived      Freq      
##  1st :8   Male  :16   Child:16   No :16   Min.   :  0.0  
##  2nd :8   Female:16   Adult:16   Yes:16   1st Qu.:  0.8  
##  3rd :8                                   Median : 13.5  
##  Crew:8                                   Mean   : 68.8  
##                                           3rd Qu.: 77.0  
##                                           Max.   :670.0
```

The above table gives a overall summary of the data. All the 4 dimensions are categorical variables thus represented as factors in data.

---

## Comprehending Information

It is very difficult to comprehend the data from this table. I developed this app to enable the user to understand the effects of these factors on the probability of survival.


The data is represented as a scatter plot of class Vs. survival probability. The user can change the age group and gender of the target group and visually observe the changes in the plot.

Survival probability is defined as the ratio of total number of people survived to the total number of passengers in that category.



----

## Insights

There are few interesting insights that could be derived from this,

1. All the children from 1st and 2nd class are survived
2. There were no child survivors from 3rd class
3. The probability of survival is much higher if you were a crew
4. Female passengers had more probability of survival than male passengers, overall
5. The chances of surviving is minimal if you were an adult traveling in first class
