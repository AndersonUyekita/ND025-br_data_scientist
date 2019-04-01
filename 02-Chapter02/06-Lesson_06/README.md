# ND025 - Supervised Learning - Lesson 06

#### Tags
* Author : AH Uyekita
* Title  :  _Ensemble Methods_
* Date   : 01/04/2019
* Course : Data Scientist Nanodegree Program
    * COD    : ND025
    * **Instructor:** Luis Serrano

***

## Ensemble Methods

This is a way to combine different methods to create a new model.

#### Bagging

It is the short of **B**oostrap **Agg**regat**ing** and usually applied any kind of aggregate function on the results of several simulations. An example for numeric values is to applied the average, on the other hand for categorical, it is possible to selected that one with higher occurency.

The result is an enhanced solution based on several complete different solutions.

#### Boosting

This one is quite similar to the Bagging, but use the concept of *Weak Learners* that stand to the specific solutions for small part of the problem. In a case of classification, it will be divided into several single splits. Later, the model will combine these weak learners to create an optimized one (or **strong learner**). The name boosting cames from the idea of Boosting the weight of each observation when it fails in the classification, which means this observation should have more weight in the next step of the model building process.

<iframe width="560" height="315" src="https://www.youtube.com/embed/LsK-xG1cLYA?controls=0" frameborder="0" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
