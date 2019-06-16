# Linear and Logistic regression model implementation

__Custom implementation of the univariate linear regression, linear logistic regression and polynomial logistic regression with regularization. Only the python `numpy` library is used along with `matplotlib` for plots in `jupyter notebook`.__

## Univariate linear regression

### Visualizing our first dataset.

<img src='img/ex1data1.png' />

#### Hypothesis function
<img src='img/' />

#### Loss/Cost function
<img src='img/' />

#### Gradient descent
<img src='img/' />

#### Loss curve and final best fit line with Gradient descent
Loss curve plotted along with the final best fit line after running 10<sup>3</sup> iterations of the Gradient descent update equations.
<img src='img/linear_regression_loss_best_line.png' />

#### Final best fit line with Normal equations method
The final best fit line after the normal equations method.
<img src='img/' />

<img src='img/linear_regression_normal_eqn_best_line.png' />

## Linear Logistic Regression

### Visualizing our second dataset.

2D representation       |  3D Representation
:----------------------:|:----------------------:
![](img/ex1data21.png)  |  ![](img/ex1data22.png)

#### Hypothesis function
<img src='img/' />

#### Loss/Cost function
<img src='img/' />

#### Gradient descent
<img src='img/' />

#### Loss curve and final boundary line using a linear function.
Here we use a linear function <img src='img/' /> to model our data. This is why our boundary line is a straight line which fits the data pretty well but we can clearly see that a polynomial model can fit the data better.

<img src='img/data1_logistic_regression_loss_contour_plot.png'/>

## Polynomial Logistic Regression

#### Loss curve and final boundary line using a polynomial function.
Here we use a polynomial hypothesis function <img src='img/' /> to model our data. Now our boundary line is a curved line which fits the data much better than the previous linear model.

<img src='img/data1_poly_logistic_regression_loss_contour_plot.png'/>


### Visualizing our third dataset.

2D representation       |  3D Representation
:----------------------:|:----------------------:
![](img/ex2data21.png)  |  ![](img/ex2data22.png)

#### Hypothesis function
<img src='img/' />

#### Loss/Cost function
<img src='img/' />

#### Gradient descent
<img src='img/' />

#### Loss curve and final boundary line using a polynomial function.
Here we use a polynomial function <img src='img/' /> to model our data.

<img src='img/data2_logistic_regression_loss_contour_plot.png'/>


## Polynomial Logistic Regression with regularization

#### Hypothesis function
<img src='img/' />

#### Loss/Cost function
<img src='img/' />

#### Gradient descent
<img src='img/' />

#### Loss curve and final boundary line using a polynomial function with regularization.
Here we use a polynomial function <img src='img/' /> to model our data. 

<img src='img/data2_regularized_logistic_regression_loss_contour_plot.png'/>


#### Acknowledgements
-   Dataset from Andrew Ng Machine Learning Stanford edu MOOC.
