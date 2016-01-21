---
title       : Phillies Stats By Year
subtitle    : Coursera Final Project
author      : JW  
job         : Developing Data Products
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : mathjax            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides

---

## An Overview of Final Shiny App

1.  The Phillies are a baseball team with a history of (mostly) futility.
2.  This shiny app provides a summary of the basic team stats by year.
3.  It also predicts the number of wins the Phillies were "expected" to have that year.


The primary source is http://www.baseball-reference.com/teams/PHI/

--- .class #id 

## Bill James
##Pioneer of Statistics in Baseball

He developed "The Pythagorean Expectation" for baseball wins.

By comparing the amount of runs a team scored in a year against the amount of runs it gives up,
a decent prediction of wins in a season is obtained.  

The formula is:

$$E(Wins) = \frac{1}{1+\Big({\frac{runs-allowed}{runs-scored}}^2\Big)}\times games$$
If the actual number of wins exceeds the predicted, the team was "lucky" or "exceeded expectation"

---

## Instructions

1.  Select a season with sliderInput() (the Phillies have existed from 1883-Present)
2.  Select a major statistic (wins, losses, etc.)
3.  The app will display your stat as well as calculate the pythagorean expected number of wins
4.  If the Phillies had won games than they were expected to, they are considered to have been "lucky"

---

## An example:

In 2006, the Phils scored 865 runs and allowed 812 runs to score.

Therefore, we would predict the team to have: 

$$E(Wins) = \frac{1}{1+\Big({\frac{812}{865}}^2\Big)}\times 162$$


```
## [1] 86.11475
```
wins

