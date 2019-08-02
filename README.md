# Linear and Logistic regression model implementation

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

**Custom implementation of the univariate linear regression, linear logistic regression and polynomial logistic regression with regularization. Only the python `numpy` library is used along with `matplotlib` for plots in `jupyter notebook`.**

## Univariate linear regression

### Visualizing our first dataset.

<img src='img/ex1data1.png' height='300' />

#### Hypothesis function

    Here, x<sub>0</sub> is always assumed to be 1

<img src='img/eq01.svg' height='20' /><br/>

    Vectorized hypothesis

<img src='img/eq02.svg' height='20' />

#### Mean Squared Error Loss function

    Also known as the MSE cost function.
    The 1/2 constant term is used to make sure the derivative smoothly cancels out the 2 term.
    Adding any constants will not affect the final minimized value of the parameters.

<img src='img/eq03.svg' height='25' /><br/>

    Vectorized MSE Loss

<img src='img/eq04.svg' height='25' />

#### Gradient descent

    The alpha term is the learning rate of the gradient descent.
    A larger alpha means larger steps at each gradient descent update but may lead to a divergence of the MSE loss.
    A very small alpha means the convergence will be inefficiently slow.

<img src='img/eq05.svg' height='25' /><br/>

    Vectorized gradient descent

<img src='img/eq06.svg' height='25' />

#### Loss curve and final best fit line with Gradient descent

Loss curve plotted along with the final best fit line after running 10<sup>3</sup> iterations of the Gradient descent update equations.
<img src='img/linear_regression_loss_best_line.png' height='380' />

#### Final best fit line with Normal equations method

The final best fit line after the normal equations method.<br/>
<img src='img/normal_equation.png' height='30'/>

<img src='img/linear_regression_normal_eqn_best_line.png' height='380' />

## Linear Logistic Regression

### Visualizing our second dataset.

|    2D representation   |    3D Representation   |
| :--------------------: | :--------------------: |
| ![](img/ex1data21.png) | ![](img/ex1data22.png) |

#### Hypothesis function

    The hypothesis function for normal linear regression is run through a non-linear function, g(z), the sigmoid function.

<img src='img/eq07.svg' height='20'/>
<img src='img/eq08.png' height='20'/>

    The sigmoid/logistic function.

<img src='img/eq09.svg' height='25'/>

#### Cost function

    The loss function is calculated using the log of maximum likelihoodsand is dependent on the true value of y.

<img src='img/eq10.png' height='48'/>

    When combined, the cost function can be expressed as:

<img src='img/eq11.svg' height='25'/>

    Vectorized cost function

<img src='img/eq12.svg' height='25'/>

#### Gradient descent

    The gradient algorithm is the similar to the one for linear regression.

<img src='img/eq13.svg' height='25'/>

    Vectorized Gradient descent

<img src='img/eq14.svg' height='25'/>

#### Loss curve and final boundary line using a linear function.

Here we use a linear function <img src='img/eq08.png' height='17'/> to model our data. This is why our boundary line is a straight line which fits the data pretty well but we can clearly see that a polynomial model can fit the data better.

<img src='img/data1_logistic_regression_loss_contour_plot.png' height='300' />

## Polynomial Logistic Regression

#### Loss curve and final boundary line using a polynomial function.

Here we use a polynomial hypothesis function <img src='img/eq16.png' height='20'/> to model our data. Now our boundary line is a curved line which fits the data much better than the previous linear model.

<img src='img/data1_poly_logistic_regression_loss_contour_plot.png' height='300' />

### Visualizing our third dataset.

|    2D representation   |    3D Representation   |
| :--------------------: | :--------------------: |
| ![](img/ex2data21.png) | ![](img/ex2data22.png) |

#### Hypothesis function

<img src='img/eq15.svg' height='20'/>

    The hypothesis function is a polynomial function of the second degree

<img src='img/eq16.png' height='25'/>
<img src='img/eq17.svg' height='30'/>

#### Cost function

    We use the same cost function for logistic regression with polynomials.

<img src='img/eq18.png' height='48'/><br/>
<img src='img/eq20.svg' height='20'/><br/>
<img src='img/eq19.svg' height='25'/><br/>
<img src='img/eq21.svg' height='25'/>

#### Gradient descent

<img src='img/eq22.svg' height='25'/><br/>

    Vectorized Gradient descent

<img src='img/eq23.svg' height='25'/>

#### Loss curve and final boundary line using a polynomial function.

Here we use a polynomial function <img src='img/eq16.png' height='20'/> to model our data.

<img src='img/data2_logistic_regression_loss_contour_plot.png' height='300' />

## Polynomial Logistic Regression with regularization

#### Loss curve and final boundary line using a polynomial function with regularization.

Here we use a polynomial function <img src='img/eq16.png' height='20'/> to model our data.

#### Cost function with regularization

    The extra term adds regularization to our regression causing our parameters to decrease in magnitude.
    The constant lambda is the regularization factor. Too large of a lambda might cause underfitting.

<img src='img/eq24.svg' height='25'/>

    Vectorized Cost function with regularization

<img src='img/eq25.png' height='35'/>

#### Gradient descent update

    We update the 0th parameter without regularization.

<img src='img/eq26.png' height='35'/>
<img src='img/eq27.svg' height='25'/>

    Vectorized gradient descent has to be done in two steps.

Calculate the gradient without regularization and update the 0<sup>th</sup> bias parameter.

<img src='img/eq28.png' height='35'/><br/>
<img src='img/eq30.png' height='25'/>

Add regularization to the gradient and then update the rest of the parameters.

<img src='img/eq29.png' height='35'/><br/>
<img src='img/eq31.png' height='25'/>

<img src='img/data2_regularized_logistic_regression_loss_contour_plot.png' height='300' />

**We can observe that the loss for training set has not quite reached the same low levels as for the logistic regression without regularization. However, our model with regularization will be more generalizable with new unseen test examples.**

#### Acknowledgements

-   Dataset from Andrew Ng Machine Learning Stanford edu MOOC.
