# Support_Vector_Regression
> Support Vector Regression (SVR) is an application of the Support Vector Machine (SVM) algorithm for regression tasks. Unlike traditional regression models that aim to minimize the error, SVR seeks to find a function that predicts within a certain margin of tolerance.

> SVR introduces a margin of tolerance (𝜖) within which predictions are considered acceptable. Data points lying outside the 𝜖-margin are called support vectors, as they determine the regression line.

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
Ordinary Least Squares helps to minimize the error between the actual value and predicted values over the regression line. That is squaring the difference between the actual value and predicted value.

## Kernel Trick:
Like SVM for classification, SVR can handle both linear and non-linear relationships by using kernel functions (e.g., linear, polynomial, radial basis function (RBF)).

## What is the Tube in SVR called?
The tube in Support Vector Regression (SVR) is commonly referred to as the epsilon-insensitive tube (or ε-tube).

## Key Details About the Epsilon-Insensitive Tube:
> + Purpose: The tube defines a margin of tolerance (𝜖) around the true target values. Predictions falling within this margin are considered acceptable and do not contribute to the error.

> + Characteristics: Data points lying inside the tube are ignored during model training, as their errors are treated as negligible.
Only points outside the tube (support vectors) influence the regression model.

> + Flexibility: The width of the tube is controlled by the hyperparameter 𝜖. A larger 𝜖 creates a wider tube, focusing on capturing general trends and ignoring small deviations. A smaller 𝜖 results in a tighter fit but increases sensitivity to noise.
