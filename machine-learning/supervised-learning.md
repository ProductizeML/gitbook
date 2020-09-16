---
description: >-
  You will learn: most-used supervised learning algorithms such as linear
  regression, logistic regression, SVM, and decision trees.
---

# Supervised Learning

## Linear Regression

**Linear regression** is a supervised machine learning algorithm where the predicted output value keeps a linear \(continuous\) relationship with the input.

#### **Example 1**

One simple application of linear regression can be used to predict the economic activity of a country in relation to its population.

![Figure 1: The regression line represents the continuous range of values between GDP as economic activity measurement and population associated.](../.gitbook/assets/screen_shot_2020-06-28_at_2.21.26_pm.png)

We can distinguish between two types:

1. **Simple** **regression**

When just considering a single variable as input data, the linear regression line can be expressed with an equation of the form:

$$
\sf{y = mx + b}
$$

Where $$m $$ and $$ b$$ are the weights our algorithm will try to “learn” to provide the most accurate predictions $$y $$ . $$x$$ represents our input data and $$y$$ represents our prediction.

Given **Exemple 1**, linear regression would let us predict the economic activity \( $$y$$ \) from the number of people \( $$x $$ \). For instance, for a region with 30 million people, the expected GDP value would be about $1,400 billion.

The same inverse logic could be applied if trying to predict the population \( $$x$$ \) from its economic activity \( $$y$$ \). In that case, we would reverse the regression equation to:

$$
\sf{x = \frac{y -b}{m}}
$$

1. **Multi-variable regression**

Following the same idea, if several variables play a role in the linear prediction, multiple weights  $$w_i$$ $$a = b$$ will apply to each variable in the following form:

$$
f(x, y, z) = w_1x + w_2y + w_3z
$$

where this time $$w_i $$are the coefficients the algorithm will try to “learn” to provide the most accurate predictions given $$x, y$$ and $$z$$ as input data.

#### Example 2

| Company | Employees | R&D Investment \($M\) | Income \($M\) | Sales \(M units\) |
| :--- | :--- | :--- | :--- | :--- |
| Company A | 15,000 | 2 | 3 | 5 |
| Company B | 30,000 | 3 | 2 | 3 |
| Company C | 10,000 | 1.5 | 1 | 2 |

In Example 2, we can still predict the sales of a company given the number of employees, investment in R&D and income as follows:

$sales\_{company D} = w\_1employees + w\_2R\&D investment + w\_3 income$

## **Loss function**

In order to find the best weights $$w_i $$ that minimizes the error between the model's predictions from its ground-truth labels, we must introduce the concept of a **loss value**. We could describe it as the absolute difference between the true value and the predicted one.

When this measurement is applied to a set of evidences, we call it **loss function** \(or **cost function**\). It can be understood as a measurement of how "good" your model is: the lower the loss, the better your model is.

For linear regression models, we typically use **Mean Squared Error** \(MSE\) as loss function:

$MSE = \frac{1}{N}\sum\_{i=1}^{n}{\(y\_i-\(mx\_i+b\)\)^2}$

where N is the total number of samples.

This way, the goal is to minimize MSE so the accuracy of the model improves. But, how this function can be minimized? The answer is via [Gradient Descent](https://www.notion.so/adriaromero/Neural-Networks-0625d8d3ce3943c5bafb21c2e8a5021a#1299c0cbd0fa4e52a7631362601e7782), covered in the [Neural Networks](https://www.notion.so/Neural-Networks-0625d8d3ce3943c5bafb21c2e8a5021a) section.

## 2. Logistic Regression

**Logistic regression** is another supervised learning method to classify samples by assigning a discrete set of classes. Similarly, as linear regression makes predictions on continuous number values, logistic regression uses a logistic **sigmoid** function as a prediction value associated with multiple variables of the form:

$y = \frac{1}{1 + e^{-z}}$

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bbcbbf13-3102-47ca-8558-57b7fb17618a/external-content.duckduckgo.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bbcbbf13-3102-47ca-8558-57b7fb17618a/external-content.duckduckgo.png)

The logistic curve of the sigmoid function for which outputs are between 0 and 1. This property allows the regression to provide a probability value.

We can distinguish between three types:

1. **Binary classification**

   This regression type only considers situations in which the observed outcome for a dependent variable only takes two types. An example case we might use logistic regression to classify lung cancer as benign or malignant.

2. **Multi-class classification**

   In this second case, the outcome can be presented as three or more types. An example case could be predicting the type of lung cancer as e.g. "cancer A", "cancer B", or "cancer C".

3. **Ordinal classification**

   Same idea as in \(2\) Multi-class classification, but this time the predictions are ordered with a sense of positioning. An example case could be a restaurant service rating choice among "poor", "fair", "good", and "excellent".

## 3. Support Vector Machines

**Support vector machines \(SVMs\)** are a set of supervised machine learning algorithms for classification, regression, and outlier detection that are built around hyperplane separation of the data. In a two dimensional space, this separation can be understood as a simple decision boundary in the form of a line, but SVMs are also effective in high dimensional spaces.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d5c71d31-7767-4c35-9511-59a1fcfc384d/Screen\_Shot\_2020-06-29\_at\_6.23.36\_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d5c71d31-7767-4c35-9511-59a1fcfc384d/Screen_Shot_2020-06-29_at_6.23.36_PM.png)

[Scikit-learn](https://scikit-learn.org/stable/modules/svm.html) SVM for a three class classification example

Thanks to their great adaptation to multidimensional spaces, SVMs are often used for Natural Language Classification problems.

## 4. Decision Trees

**Decision trees** are non-parametric supervised machine learning techniques that are able to make predictions by learning simple decision rules encoded in a flowchart-like structure.

These tree structures are easy to represent and interpret. Leaves on the tree represent classifications labels, non-leaf nodes are features, and branches represent conjunctions of features that lead to the classifications.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c2a136d1-a4ae-4128-92b8-1af07c24a514/3-s2.0-B978012817358900010X-gr007.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c2a136d1-a4ae-4128-92b8-1af07c24a514/3-s2.0-B978012817358900010X-gr007.jpg)

An example of a decision tree with the objective of predicting if the weather is good or not for a hike. Source: [https://www.sciencedirect.com/topics/computer-science/decision-trees](https://www.sciencedirect.com/topics/computer-science/decision-trees)

When grouping multiple decision trees together, we refer to this ensemble of models as **random forests**.

