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
17. After splitting, Information Gain is more than that of the parent node. What does this mean?
- High information gain means higher the homogeneity of nodes after the split.
18. Can information gain be used for continuous target variable?
- Gini, Chi-square and Information gain; all three techniques are used in the case of categorical target variable only.
19. _____ the entropy, _____ would be the information gain.
- The relation between entropy and information gain is: Information gain = 1 - Entropy. Hence, lower the entropy higher would be the IG and vice versa.
20. Let's say you are asked to work on a problem to predict the future sales of a product in a store and decided to use a decision tree model. Which algorithm should be used for splitting?
- Since sales is a continuous variable, so the reduction in variance technique should be used for splitting. Rest all are for categorical variables
21. If a node has the same values or the node is purely homogeneous, the variance of the node would be?
- Since the node has all similar values, the variance of the node would be 0.
22. We select a variable having higher variance for the splitting?
- A node having high variance means it is more impure. Since we seek the pure nodes after the splitting, the variable having low variance should be selected.
23. In Decision trees, which of the parameter(s) can help to prevent overfitting?
- Max depth
- Minimum samples for node split
- Minimum samples for leaf node
24. What is the maximum number of terminal nodes in a decision tree if our training dataset has N samples?
- N
25. What is feature engineering?
- Feature engineering is the process of extracting information from the existing data in order to improve the performance of the model.
26. Feature transformation is used for transforming non-linear data to linear and also to reduce the skewness of the variable.
27. Log transformation is used for removing right skewness from the data.
28. Feature transformation changes the distribution of the variable.
29. Changing the scale of the data does not affect the distribution as scaling just changes the range of the data.
30. Why do we need to combine sparse classes?
- To reduce the no. of categories.
31. What is binning?
- Binning or discretization is the process of transforming numeric variables into categorical.
32. While generating new features using the Feature Interaction method, we always use two categorical variables. True or false?
- We can use any number of features or columns while performing feature interaction.
33. Why do we need joins?
- Joins are used in SQL to combine multiple tables.
34. The most common used join in data science applications is?
- The left join.
35. How many left joins can be done in a single SQL query?
- You can add any number of joins clauses in SQL query.
36. Only one type of join can be done in one query?
- False
37. Which is the most time consuming join?
- Cross join, since it tries to match all combinations of keys of first and second table
38. Indexing can be done on?
- Indexing can be done only on one table as per SQL at a time, it can be done on multiple fields using composite key(s).
39. The LIKE operator is used to do what?
- LIKE is an operator which is used to do pattern matching based on regular expressions in SQL.
40. What is the primary daemon process of MongoDB?
- mongod is the primary daemon process of MongoDB that implements the queries in MongoDB.
41. What is the interactive shell for MongoDB?
- mongo is the interactive shell provided by MongoDB to implement queries in MongoDB.
42. What is the default port on which the local MongoDB server opens up?
- The default MongoDB server opens up on the port 27017.
 
