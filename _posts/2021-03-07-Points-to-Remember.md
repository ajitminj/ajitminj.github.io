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

3. Sigmoid function transforms a linear line into a curve which has values between 0 and 1.
- This is true. The reason we choose a sigmoid function to model classification problems solved with logistic regression is that we want to make sure that the predicted value has a defined range which helps in differentiating the classes.

4. Ridge regression helps in pushing the insignificant independent variables to absolute zero. True or False?
- False

5. Lasso regularization is useful when only a small subset of independent variables is significant in the predictive process. True or False?
- True
