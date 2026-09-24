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

## Loss function

The mean squared error loss function measures the average squared difference between the predicted and actual values:

`J(theta, c) = (1 / m) * sum((theta * x_i + c - y_i)^2)`

where `m` is the number of data points, `x_i` is an input value, `y_i` is the actual value, and `theta * x_i + c` is the prediction. A lower loss means that the model predictions are closer to the actual values.

## Gradient function

The gradient function calculates how much the slope and intercept should change:

`dJ/dtheta = (1 / m) * sum((theta * x_i + c - y_i) * x_i)`

`dJ/dc = (1 / m) * sum(theta * x_i + c - y_i)`

Gradient descent then updates the parameters using the learning rate `alpha`:

`theta = theta - alpha * dJ/dtheta`

`c = c - alpha * dJ/dc`

The notebook uses `gradient_function()` to calculate both gradients during every training epoch.

## What was used and how

- **Python:** Used as the programming language for loading data, defining functions, training the model, and creating predictions.
- **pandas:** Used `read_csv()` to load `data.csv` into a DataFrame and inspect the dataset with `columns`, `head()`, and `shape`.
- **NumPy:** Used `array()` to convert the `Hours` and `Scores` columns into numerical arrays for calculations.
- **Matplotlib:** Used `scatter()` to show the data, `plot()` to draw the regression line, and additional plots to show loss during training and parameter changes.
- **CSV dataset:** The `Hours` column is the input feature, and the `Scores` column is the target value the model learns to predict.
- **Gradient descent:** Used repeatedly for the configured number of epochs. Each epoch calculates the gradients, updates `theta` and `c`, and stores the current loss in `grad_mse`.
- **Notebook:** `myine.ipynb` keeps the code, explanations, calculations, and visual results together so the learning process can be followed step by step.

## Gradient descent settings

- `theta = 0`: initial slope
- `c = 0`: initial intercept
- `epochs = 100`: number of training iterations
- `alpha = 0.001`: learning rate

During each epoch, the model calculates the error, finds the parameter update rates, and adjusts `theta` and `c`. The goal is to minimize the mean squared error.

## Files

- `myine.ipynb`: notebook containing the implementation and plots.
- `data.csv`: dataset containing `Hours` and `Scores`.
