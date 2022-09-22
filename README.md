# Simple-Linear-Regression

## What is Regression?
Regression models describe the relationship between variables by fitting a line to the observed data. Linear regression models use a straight line, while logistic and nonlinear regression models use a curved line. Regression allows you to estimate how a dependent variable changes as the independent variable(s) change.

## Understanding Linear Regression

In the most simple words, Linear Regression is the supervised Machine Learning model in which the model finds the best fit linear line between the independent and dependent variable i.e it finds the linear relationship between the dependent and independent variable.

Linear Regression is of two types: Simple and Multiple. Simple Linear Regression is where only one independent variable is present and the model has to find the linear relationship of it with the dependent variable

Simple linear regression is used to estimate the relationship between two quantitative variables. You can use simple linear regression when you want to know:

-How strong the relationship is between two variables (e.g. the relationship between rainfall and soil erosion).

-The value of the dependent variable at a certain value of the independent variable (e.g. the amount of soil erosion at a certain level of rainfall).

Equation of Simple Linear Regression, where bo is the intercept, b1 is coefficient or slope, x is the independent variable and y is the dependent variable.

Y=b0 +b1x

Whereas, In Multiple Linear Regression there are more than one independent variables for the model to find the relationship.

Equation of Multiple Linear Regression, where bo is the intercept, b1,b2,b3,b4…,bn are coefficients or slopes of the independent variables x1,x2,x3,x4…,xn and y is the dependent variable.

Y=b0+b1x1+b2x2+b3x3+......bnxn

A Linear Regression model’s main aim is to find the best fit linear line and the optimal values of intercept and coefficients such that the error is minimized.

Error is the difference between the actual value and Predicted value and the goal is to reduce this difference.

Let’s understand this with the help of a diagram.

![image](https://user-images.githubusercontent.com/109084435/191804869-a0bf172e-cea8-44b9-84b3-4df61799dae9.png)

Image Source: Statistical tools for high-throughput data analysis

In the above diagram,

-x is our dependent variable which is plotted on the x-axis and y is the dependent variable which is plotted on the y-axis.

-Black dots are the data points i.e the actual values.

-bo is the intercept which is 10 and b1 is the slope of the x variable.

-The blue line is the best fit line predicted by the model i.e the predicted values lie on the blue line.

The vertical distance between the data point and the regression line is known as error or residual. Each data point has one residual and the sum of all the differences is known as the Sum of Residuals/Errors. 

### Assumptions of Linear Regression
The basic assumptions of Linear Regression are as follows:

##### 1. Linearity: 

It states that the dependent variable Y should be linearly related to independent variables. This assumption can be checked by plotting a scatter plot between both variables.

![image](https://user-images.githubusercontent.com/109084435/191805576-0c20763f-13ee-4ead-9a88-4a067e4cf7ca.png)

##### 2. Normality:

The X and Y variables should be normally distributed. Histograms, KDE plots, Q-Q plots can be used to check the Normality assumption. 

![image](https://user-images.githubusercontent.com/109084435/191805733-f92a3014-b123-43db-b66b-53b91b1191df.png)

##### 3. Homoscedasticity: 

The variance of the error terms should be constant i.e the spread of residuals should be constant for all values of X. This assumption can be checked by plotting a residual plot. If the assumption is violated then the points will form a funnel shape otherwise they will be constant.

![image](https://user-images.githubusercontent.com/109084435/191805820-0bf3a8ae-1015-4dd6-86c7-63896f32fe59.png)

##### 4. Independence/No Multicollinearity:

The variables should be independent of each other i.e no correlation should be there between the independent variables. To check the assumption, we can use a correlation matrix or VIF score. If the VIF score is greater than 5 then the variables are highly correlated.

In the below image, a high correlation is present between x5 and x6 variables.

![image](https://user-images.githubusercontent.com/109084435/191805953-4b503668-4913-4d88-83a8-ae5ee8babbd1.png)

##### 5. The error terms should be normally distributed.

Q-Q plots and Histograms can be used to check the distribution of error terms.

![image](https://user-images.githubusercontent.com/109084435/191806048-47f1d1ee-be37-4d11-9660-8a8ba31974ec.png)

##### 6. No Autocorrelation:

The error terms should be independent of each other. Autocorrelation can be tested using the Durbin Watson test. The null hypothesis assumes that there is no autocorrelation. The value of the test lies between 0 to 4. If the value of the test is 2 then there is no autocorrelation.

![image](https://user-images.githubusercontent.com/109084435/191806717-34cee30a-e34f-46a3-8c74-970baab66414.png)

### Evaluation Metrics for Regression Analysis

To understand the performance of the Regression model performing model evaluation is necessary. Some of the Evaluation metrics used for Regression analysis are:

##### 1. R squared or Coefficient of Determination:

The most commonly used metric for model evaluation in regression analysis is R squared. It can be defined as a Ratio of variation to the Total Variation. The value of R squared lies between 0 to 1, the value closer to 1 the better the model.

![image](https://user-images.githubusercontent.com/109084435/191807087-50b2d762-0632-4348-b043-13f091506b81.png)

where SSRES is the Residual Sum of squares and SSTOT is the Total Sum of squares

##### 2. Adjusted R squared:

It is the improvement to R squared. The problem/drawback with R2 is that as the features increase, the value of R2 also increases which gives the illusion of a good model. So the Adjusted R2 solves the drawback of R2. It only considers the features which are important for the model and shows the real improvement of the model.

Adjusted R2 is always lower than R2.

![image](https://user-images.githubusercontent.com/109084435/191807673-5eec6acb-186f-48d6-9011-ddd956938c80.png)

##### 3. Mean Squared Error (MSE):

Another Common metric for evaluation is Mean squared error which is the mean of the squared difference of actual vs predicted values.

![image](https://user-images.githubusercontent.com/109084435/191807858-c110d33e-deca-4bb2-9c89-a013133e9164.png)

##### 4. Root Mean Squared Error (RMSE):

It is the root of MSE i.e Root of the mean difference of Actual and Predicted values. RMSE penalizes the large errors whereas MSE doesn’t

![image](https://user-images.githubusercontent.com/109084435/191808014-a5050c30-2eb2-4b78-b9d7-0f5b5ea8094e.png)

