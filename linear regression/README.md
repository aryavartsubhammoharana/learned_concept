# Linear Regression

This folder contains my learned concept and implementation of simple linear regression using Python.

## What I learned

- How to load a CSV dataset with pandas.
- How to inspect data using columns, `head()`, and `shape`.
- How to select input and target values from a DataFrame.
- How to visualize the relationship between study hours and scores with a scatter plot.
- How a linear regression model uses the equation:

  `y = theta * x + c`

  where `theta` is the slope and `c` is the intercept.

- How to initialize model parameters and training settings.
- How to calculate the mean squared error (MSE) cost function.
- How gradient descent updates the slope and intercept to reduce the cost.
- How to plot the final regression line against the original data.
- How to visualize the relationship between the cost and the model parameters.

## Gradient descent settings

- `theta = 0`: initial slope
- `c = 0`: initial intercept
- `epochs = 100`: number of training iterations
- `alpha = 0.001`: learning rate

During each epoch, the model calculates the error, finds the parameter update rates, and adjusts `theta` and `c`. The goal is to minimize the mean squared error.

## Files

- `myine.ipynb`: notebook containing the implementation and plots.
- `data.csv`: dataset containing `Hours` and `Scores`.
