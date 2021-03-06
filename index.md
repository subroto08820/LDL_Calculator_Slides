---
title       : LDL Cholestorol Calculator
subtitle    : 
author      : Subrata Mukherjee
job         : Developing Data Products - Slidify presentation
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [bootstrap,mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
logo        : logo.png
---

## LDL Cholestorol 

There are primarily two methods for computing LDL Cholestorol based on TC (Total Cholestorol), HDL (HDL Cholestorol) and TG (Triglycerides). 


1. Friedewald (1972) Formula
2. "Iranian" (2008) Formula

---

## Friedewald (1972) Formula

Using Friedewald Formula, LDL Cholesterol is calculated as below:
 
$${TC - HDL - {TG/5.0}}$$     
Here TC  = Total Cholesterol (mg/dL), HDL = HDL Cholesterol (mg/dL) and TG  = Triglycerides (mg/dL).

In the Test Case below, using TC=201, HDL=74 and TG=44, ensure that calculated value of LDL Cholesterol=118.2 (note: all the figures are in (mg/dL)).


```r
TC <- 201
HDL <- 74
TG <- 44
round(TC - HDL - (TG / 5), 1)
```

```
## [1] 118.2
```


      

---

## "Iranian" (2008) Formula

The "Iranian" formula was made with people having elevated cholesterol in mind and can perhaps give a better "estimation" of LDL when our Triglycerides are nice and low. Using "Iranian" Formula, LDL Cholesterol is calculated as below:

$${{TC/1.19} + {TG/1.9} - {HDL/1.1} - 38}$$   

In the Test Case below, using TC=201, HDL=74 and TG=44, ensure that calculated value of LDL Cholesterol=86.8 (note: all the figures are in (mg/dL)).


```r
TC <- 201
HDL <- 74
TG <- 44
round(TC/1.19 + TG/1.9 - HDL/1.1 - 38, 1)
```

```
## [1] 86.8
```

 

---

## Thanks and feedback location

I hope this presentation helps you understand how LDL Cholesterol can be computed using either of the two formula.

Please direct your feedback to subroto08820@gmail.com 

Thanks you for your time.
