# Support_Vector_Regression
> Support Vector Regression (SVR) is an application of the Support Vector Machine (SVM) algorithm for regression tasks. Unlike traditional regression models that aim to minimize the error, SVR seeks to find a function that predicts within a certain margin of tolerance.

> SVR introduces a margin of tolerance (𝜖) within which predictions are considered acceptable. Data points lying outside the 𝜖-margin are called support vectors, as they determine the regression line..

## Advantages of SVR
> + Effective with High Dimensions:
Handles high-dimensional data efficiently, especially with kernel tricks.

> + Robust to Outliers:
Focuses on data within the 𝜖-margin, ignoring small deviations.

> + Non-Linear Relationships:
Models complex, non-linear relationships through kernels.

## Disadvantages of SVR
> + Computational Complexity:
Training can be slow for large datasets due to quadratic optimization.
> + Scalability:
May struggle with very large datasets.
> + Parameter Tuning:
Requires careful tuning of hyperparameters (𝜖, and kernel parameters).

### Note:
Ordinary Least Squares helps to minimize the error between the actual value and predicted values over the regression line. That is squaring the difference between the actual value and predicted value. Any points outside the tube is regarded as the support vector

## Kernel Trick:
Like SVM for classification, SVR can handle both linear and non-linear relationships by using kernel functions (e.g., linear, polynomial, radial basis function (RBF)).

## What is the Tube in SVR called?
The tube in Support Vector Regression (SVR) is commonly referred to as the epsilon-insensitive tube (or ε-tube).
> + The points inside the tube can be seen as the margin error we allow our model to have.
> + The points outside the tube are cared about. The distance between the tube and the points outside is calculated unlike the OLS where the distance between the points and the predicted values (line) is calculated.
>
## Slack Variable
> In Support Vector Regression (SVR), slack variables (𝜉𝑖  and 𝜉𝑖∗ ) are used to handle data points that fall outside the epsilon-insensitive tube. These variables allow the model to tolerate deviations beyond the margin of tolerance (𝜖) while still optimizing the regression function.

[Click to view diagram for slack variable](https://ibb.co/xgzH9mc)

## Key Concepts of Slack Variables
>What Are Slack Variables?

> 𝜉𝑖  measures how much a data point exceeds the upper boundary of the epsilon-insensitive tube.

> 𝜉𝑖∗ measures how much a data point falls below the lower boundary of the tube.

## Purpose of Slack variable
> + Handling Outliers: Slack variables help in dealing with outliers and data points that don't fit well within the tube. If a data point falls outside the tube, the slack variable quantifies the degree to which the prediction is incorrect.

> + Allowing Flexibility: Without slack variables, the model would be forced to fit the data perfectly within the margin, which could lead to overfitting, especially in noisy datasets. Slack variables allow the model to tolerate deviations, ensuring better generalization.

## Key Details About the Epsilon-Insensitive Tube:
> + Purpose: The tube defines a margin of tolerance (𝜖) around the true target values. Predictions falling within this margin are considered acceptable and do not contribute to the error.

> + Characteristics: Data points lying inside the tube are ignored during model training, as their errors are treated as negligible.
Only points outside the tube (support vectors) influence the regression model.

> + Flexibility: The width of the tube is controlled by the hyperparameter 𝜖. A larger 𝜖 creates a wider tube, focusing on capturing general trends and ignoring small deviations. A smaller 𝜖 results in a tighter fit but increases sensitivity to noise.

## Mathematical computation - SVR
[See the formula here! Click to View](https://ibb.co/KqH9c6Z)

### Where:
+ w is the weight vector of the model.
+ 𝐶 is the regularization parameter, which determines the penalty for violating the 𝜖-insensitive tube.
+ ξi  and 𝜉𝑖∗  are the slack variables that represent how much the 𝑖-th data point deviates from the tube.

### This is linear type
