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

6. What do we mean by the process of dimensionality reduction?
- Dimensionality reduction is a process of eliminating independent variables such that the maximum information is retained with limited variables.

7. Missing value ratio and forward feature selection are feature selection techniques whereas PCA is feature extraction technique.
8. Feature selection keeps a subset of the original features while feature extraction creates new features using the existing features.
9. Why do we use the low variance filter?
- Variables with low variance do not contain any significant information. 
10. How do we apply a high correlation filter?
- We calculate the correlation between independent variables and among the two correlated variables, the variable having less correlation with the target variable get dropped.
11. While checking the correlations among the variables we should look for high positively correlated features?
- This is false because we’re more concerned about the magnitude of the correlation rather than the sign. So both, high positively and negatively correlated variables should be taken into account.
12. In decision trees, What is the basic idea behind choosing the best split in the data?
- Resultant nodes should be as homogeneous as possible.
13. What does an ideal pure node have?
- 100% of one class and 0 of other classes.
14. Gini can be used for multiclass classification problems.
- True
15. What does Gini value of 1 represent?
- The nodes are homogeneous
16. What does a high value of Chi-square indicate?
- Node distribution is very different from parent node
- Node is more homogeneous than the parent

