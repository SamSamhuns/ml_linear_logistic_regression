# Linear and Logistic regression model implementation

__Custom implementation of the univariate linear regression, linear logistic regression and polynomial logistic regression with regularization. Only the python `numpy` library is used along with `matplotlib` for plots in `jupyter notebook`.__

## Univariate linear regression

### Visualizing our first dataset.

<img src='img/ex1data1.png' height='380' />

#### Hypothesis function
<img src='img/eq01.svg' height='25' /><br/>
<img src='img/eq02.svg' height='30' />

#### Loss/Cost function
<img src='img/eq03.svg' height='30' /><br/>
<img src='img/eq04.svg' height='30' />

#### Gradient descent
<img src='img/eq05.svg' height='30' /><br/>
<img src='img/eq06.svg' height='30' />

#### Loss curve and final best fit line with Gradient descent
Loss curve plotted along with the final best fit line after running 10<sup>3</sup> iterations of the Gradient descent update equations.
<img src='img/linear_regression_loss_best_line.png' height='380' />

#### Final best fit line with Normal equations method
The final best fit line after the normal equations method.
<img src='img/normal_equation.png' height='30'/>

<img src='img/linear_regression_normal_eqn_best_line.png' height='380' />

## Linear Logistic Regression

### Visualizing our second dataset.

2D representation       |  3D Representation
:----------------------:|:----------------------:
![](img/ex1data21.png)  |  ![](img/ex1data22.png)

#### Hypothesis function
<img src='img/eq07.svg' height='25'/>
<img src='img/eq08.png' />
<img src='img/eq09.svg' height='35'/>

#### Loss/Cost function
<img src='img/eq10.png' height='75'/>
<img src='img/eq11.svg' height='75'/>
<img src='img/eq12.svg' height='75'/>

#### Gradient descent
<img src='img/eq13.svg' height='35'/>
<img src='img/eq14.svg' height='35'/>

#### Loss curve and final boundary line using a linear function.
Here we use a linear function <img src='img/' /> to model our data. This is why our boundary line is a straight line which fits the data pretty well but we can clearly see that a polynomial model can fit the data better.

<img src='img/data1_logistic_regression_loss_contour_plot.png' height='380' />

## Polynomial Logistic Regression

#### Loss curve and final boundary line using a polynomial function.
Here we use a polynomial hypothesis function <img src='img/' /> to model our data. Now our boundary line is a curved line which fits the data much better than the previous linear model.

<img src='img/data1_poly_logistic_regression_loss_contour_plot.png' height='380' />


### Visualizing our third dataset.

2D representation       |  3D Representation
:----------------------:|:----------------------:
![](img/ex2data21.png)  |  ![](img/ex2data22.png)

#### Hypothesis function
<img src='img/eq15.svg' height='25'/>
<img src='img/eq16.svg' height='35'/>
<img src='img/eq17.svg' height='35'/>

#### Loss/Cost function
<img src='img/eq18.png' height='65'/>
<img src='img/eq19.svg' height='35'/>
<img src='img/eq20.svg' height='35'/>
<img src='img/eq21.svg' height='35'/>

#### Gradient descent
<img src='img/eq22.svg' height='35'/>
<img src='img/eq23.svg' height='35'/>

#### Loss curve and final boundary line using a polynomial function.
Here we use a polynomial function <img src='img/' /> to model our data.

<img src='img/data2_logistic_regression_loss_contour_plot.png' height='380' />

## Polynomial Logistic Regression with regularization

#### Loss curve and final boundary line using a polynomial function with regularization.
Here we use a polynomial function <img src='img/' /> to model our data.

#### Loss function with regularization
<img src='img/eq24.svg' height='55'/>
<img src='img/eq25.png' height='55'/>

#### Gradient descent update
<img src='img/eq26.svg' height='55'/>
<img src='img/eq27.svg' height='55'/>
<img src='img/eq28.png' height='55'/>

<img src='img/data2_regularized_logistic_regression_loss_contour_plot.png' height='380' />

#### Acknowledgements
-   Dataset from Andrew Ng Machine Learning Stanford edu MOOC.
