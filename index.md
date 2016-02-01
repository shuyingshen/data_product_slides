---
title       : Predicting Miles per Gallon
subtitle    : Developing Data Product Project
author      : Shuying Shen
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## How much MPG?

Miles per Gallon depends on multiple factors. These factors include but not limit to:

1. Weight of the car
2. Transmission type
3. Number of cylinders

---

## MPG prediction made simple!

Now you can enter the weight, transmission type and number of cylinders and get MPG estimates in a simple and interactive fashion.

This prediction model is developed from Motor Trend Car Road Tests dataset (mtcars). Here's the summary information of the model:

```r
model = lm(mpg~wt+am+as.factor(cyl)+wt:am, data=mtcars)
summary(model)$coef
```

```
##                  Estimate Std. Error   t value     Pr(>|t|)
## (Intercept)     29.774836  2.8403415 10.482836 7.870715e-11
## wt              -2.398713  0.8439884 -2.842116 8.603904e-03
## am              11.568790  4.0877912  2.830083 8.853842e-03
## as.factor(cyl)6 -2.709777  1.3573517 -1.996370 5.646509e-02
## as.factor(cyl)8 -4.776110  1.5558306 -3.069814 4.964603e-03
## wt:am           -4.067981  1.3974151 -2.911075 7.295503e-03
```

--- 

## Here's how to use the tool

First go to [https://shuying.shinyapps.io/project/](https://shuying.shinyapps.io/project/) and give it a try! You can:

1. Enter a value for weight (assuming you are a reasonable person and do not believe in cars with negative weight). 
2. Choose the transmission type to be manual or automatic, and 
3. number of cylinders to be 4, 6 or 8. 
4. Once you hit the "submit" button. VOILA!

--- 

## Questions?

Thank you for trying this product out!

If you are interested in the codes that generated the product, please go to [https://github.com/shuyingshen/develop_data](https://github.com/shuyingshen/develop_data) for detail information. 



