# Linear Regression

#### Welcome to My first blog !!!!!!

In many cases you don't need to know the Implementation details of algorithm. However, having good understanding of how algorithm performs in backend will help you to choose best alogorithm to the usecase and it also helps you to optimize it. (by performing hyper- parameter tuning)

In this blog, we will explore how Linear Regression will work. Most of us know how to implement Linear Regression algorithm by simply importing from Scikit-Learn Library, lets see what is the math behind the algo. I'm assuming that all are familiar with vectors and matrices and, how to transpose them, multiply them, and inverse them, and what partialderivatives are..

## What is Regression analysis?

Regression analysis is a way of mathematically sorting out which of those variables does indeed have an impact. It answers the questions: 

- Which factors matter most? 
- Which can we ignore? 
- How do those factors interact with each other? 
- Most importantly, how certain are we about all of these factors?

By using Linear models we can forecast the future analysis. Okay, lets jump into the Liner Regression


## Linear Regression

Linear Regression is a simple linear model which makes prediction by computing weighted sum of input features plus a bias term.

Linear Regression model prediction : 

- y = b + m1x1 + m2x2 + ⋯ + mnxn

Okay, this is the equation of the Linear Regression. Now, we have a question How do we train it?

- Training a model means adjusting the weights of inputs in such a way that the model best fits the training set. Now the question arises is How do we adjust the weights of inputs.

- Performing Linear regression using Scikit-Learn is quite simple, lets see what is the math behind it.
```
from sklearn.linear_model import LinearRegression
lin_reg = LinearRegression()
lin_reg.fit(X, y)
```

Linear Regression class is based up on the **scipy.linalg.lstsq()** function, Which computes the weights by pseudoinverse of input

- `m = X' y  - Where X' is pseudoinverse of X and the pseudoinverse is computed using Standard matrix factorization technique called SVD (Singular Value Decomposition)` 

```
# We can use np.linalg.pinv() to compute pseudoinverse directly

np.linalg.pinv(X).dot(y)
```

**Thanks for reading** in next blog we will see different ways to train a Linear regression model.