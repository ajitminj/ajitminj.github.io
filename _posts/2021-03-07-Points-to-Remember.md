---
title: "Points to Remember"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Machine learning
  - Notes
---

1. What is the problem with linear regression when the number of predictors start increasing?
- As the number of predictors start to increase the linear regression model starts to overfit the data and starts capturing all the data points including the noise.

2. Let's say you are asked to predict whether a person has diabetes or not. You applied logistic regression since the dependent variable is yes or no. Which method will    you use to evaluate your model?
- Since we would like to minimize the false negatives which means the number of people having diabetes predicted as they don’t have, Recall should be used as evaluation   metrics.
