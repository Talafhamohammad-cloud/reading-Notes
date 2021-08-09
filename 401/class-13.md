# linear regression :

## What is Linear Regression?
Linear regression is a basic and commonly used type of predictive analysis.  The overall idea of regression is to examine two things: (1) does a set of predictor variables do a good job in predicting an outcome (dependent) variable?  (2) Which variables in particular are significant predictors of the outcome variable, and in what way do they–indicated by the magnitude and sign of the beta estimates–impact the outcome variable?  These regression estimates are used to explain the relationship between one dependent variable and one or more independent variables.  The simplest form of the regression equation with one dependent and one independent variable is defined by the formula y = c + b*x, where y = estimated dependent variable score, c = constant, b = regression coefficient, and x = score on the independent variable.
Naming the Variables.  There are many names for a regression’s dependent variable.  It may be called an outcome variable, criterion variable, endogenous variable, or regressand.  The independent variables can be called exogenous variables, predictor variables, or regressors.
Three major uses for regression analysis are (1) determining the strength of predictors, (2) forecasting an effect, and (3) trend forecasting.


## Types of Linear Regression:
-Simple linear regression
1 dependent variable (interval or ratio), 1 independent variable (interval or ratio or dichotomous)
-Multiple linear regression
1 dependent variable (interval or ratio) , 2+ independent variables (interval or ratio or dichotomous)
-Logistic regression
1 dependent variable (dichotomous), 2+ independent variable(s) (interval or ratio or dichotomous)
-Ordinal regression
1 dependent variable (ordinal), 1+ independent variable(s) (nominal or dichotomous)
-Multinomial regression
1 dependent variable (nominal), 1+ independent variable(s) (interval or ratio or dichotomous)
-Discriminant analysis
1 dependent variable (nominal), 1+ independent variable(s) (interval or ratio)

## Simple Linear Regression With scikit-learn
There are five basic steps when you’re implementing linear regression:

1- Import the packages and classes you need.
2- Provide data to work with and eventually do appropriate transformations.
3- Create a regression model and fit it with existing data.
4- Check the results of model fitting to know whether the model is satisfactory.
5- Apply the model for predictions.
