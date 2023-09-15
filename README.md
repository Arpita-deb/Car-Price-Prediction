# Predicting Car Prices
## Linear Regression and Hypothesis Testing use case
# Linear Regression

Linear Regression is a technique that estimates the linear relationship between a continuous dependent variable and one or more independent variables.This technique is applicable for Supervised learning Regression problems where we try to predict a continuous variable.

Linear Regression can be further classified into two types – Simple and Multiple Linear Regression. In this project, I employ Simple Linear Regression technique where I have one independent and one dependent variable. It is the simplest form of Linear Regression where we fit a straight line to the data.

In this project -
* We want to find out if there is any correlation between these two variables
* We will find the best fit line for the dataset.
* How the dependent variable is changing by changing the independent variable.

For linear regression model, we need to first identify the dependent and independent variables.
* **Dependent/Predictor variable (y)** : 'price'
* **Independent variable (x)** : 'engine_size'

## 1.a Simple Linear Regression (SLR)

Simple Linear Regression (or SLR) is the simplest model in machine learning. It models the linear relationship between the independent and dependent variables.

![SLR](https://static.javatpoint.com/tutorial/machine-learning/images/linear-regression-in-machine-learning.png)

In this project, there is one independent or input variable which represents the Car engine size data and is denoted by X. Similarly, there is one dependent or output variable which represents the Car price data and is denoted by y. We want to build a linear relationship between these variables. This linear relationship can be modelled by mathematical equation of the form:-

             Y = β0   + β1*X    -------------   (1)


In this equation, X and Y are called independent and dependent variables respectively,

β1 is the coefficient for independent variable (slope) and

β0 is the intercept term.

β0 and β1 are called parameters of the model.

In this Simple Linear Regression model, we want to fit a line which estimates the linear relationship between X and Y. So, the question of fitting reduces to estimating the parameters of the model β0 and β1.

### Ordinary Least Square Method

Ordinary least squares estimates the beta coefficients in a linear regression model by minimizing a measure of error called the sum of squared residuals.

As I have described earlier, the Sales and Advertising data are given by X and y respectively. We can draw a scatter plot between X and y which shows the relationship between them.

Now, our task is to find a line which best fits this scatter plot. This line will help us to predict the value of any Target variable for any given Feature variable. This line is called Regression line.

We can define an error function for any line. Then, the regression line is the one which minimizes the error function. Such an error function is also called a Loss function.

### Loss function: 

A function that measures the distance between observed  values and the model’s estimated values.
We want the Regression line to resemble the dataset as closely as possible. In other words, we want the line to be as close to actual data points as possible. It can be achieved by minimizing the vertical distance between the actual data point and fitted line. I calculate the vertical distance between each data point and the line. This distance is called the residual.

![Lf](https://th.bing.com/th/id/R.880549d05c57fe96ababcb9ed4d9dd50?rik=YPuUc37DFkJSUQ&riu=http%3a%2f%2fwww.sthda.com%2fenglish%2fsthda-upload%2fimages%2fmachine-learning-essentials%2flinear-regression.png&ehk=svAm3xChWZwytrdGETUS%2fRhwtmbJuBtgZYcEOu3RkVQ%3d&risl=&pid=ImgRaw&r=0)

So, in a regression model, we try to minimize the residuals by finding the line of best fit. The residuals are represented by the vertical dotted lines from actual data points to the line.

We can try to minimize the sum of the residuals, but then a large positive residual would cancel out a large negative residual. For this reason, we minimize the sum of the squares of the residuals.

Mathematically, we denote actual data points by yi and predicted data points by ŷi. So, the residual for a data point i would be given as di = yi - ŷi

Sum of the squares of the residuals is given as:

			D = Ʃ di**2       for all data points


This is the Cost function. It denotes the total error present in the model which is the sum of the total errors of each individual data point.

We can estimate the parameters of the model β0 and β1 by minimizing the error in the model by minimizing D. Thus, we can find the regression line given by equation (1).

This method of finding the parameters of the model and thus regression line is called Ordinary Least Square Method.

## Assumptions of Linear Regression Model:

1. **Linear relationship**: There exists a linear relationship between the independent variable, x, and the dependent variable, y.

2. **Independence**: The residuals are independent. In particular, there is no correlation between consecutive residuals in time series data.

3. **Homoscedasticity**: The residuals have constant variance at every level of x.

4. **Normality**: The residuals of the model are normally distributed.

Multiple Linear Regression Model 

Multiple Linear Regression is one of the important regression algorithms which models the linear relationship between a single dependent continuous variable and more than one independent variable.

For MLR, the dependent or target variable(Y) must be the continuous/real, but the predictor or independent variable may be of continuous or categorical form.
Each feature variable must model the linear relationship with the dependent variable.
MLR tries to fit a regression line through a multidimensional space of data-points.
# Plan:

### Goals:

a. To build a model that relates price to the other variables listed above. Write the estimated regression equation.

b. Is the model statistically significant at the α = .05 level? Write out the null and alternative hypotheses, the appropriate test statistic, the p-value for that test statistic and your conclusion, based on that p-value.

c. The automobile company suspects that vehicle price depends on engine size, holding everything else equal. To evaluate this suspicion, write out the null and alternative hypotheses, the appropriate test statistic, the p-value for that test statistic and your conclusion based on that p-value, at the α = .05 level.

d. The automobile company also suspects that prices are different for turbocharged cars, holding everything else equal. Interpret the slope of turbo to determine whether the sample data supports this suspicion. Specifically, report the appropriate test statistic, the p-value for that test statistic and your conclusion, based on that p-value, at the α = .05 level.

### About the dataset: 
The dataset contains 205 instances(rows) with 26 features of car models from 1985 Ward's Automotive Yearbook.

### Data Integrity and Validation:

* Reliability:
* Originality:
* Comprehensiveness:
* Citation:
* Current:

### Data Dictionary:
| Column Name | Data Type | Column Description |
| :--- | :--- | :--- |
| Car_ID | int | Unique id of each observation	|	
| Symboling | int64 |	Its assigned insurance risk rating, A value of +3 indicates that the auto is risky, -3 that it is probably pretty safe |	
| carCompany | object | Name of car company |
| fueltype | object | Car fuel type i.e gas or diesel |
| aspiration | object | Aspiration used in a car |
| doornumber | object | Number of doors in a car |	
| carbody | object |	Body of car (hardtop, wagon, sedan, hatchback, convertible) |
| drivewheel | object | Type of drive wheel (4wd, fwd, rwd) |	
| enginelocation | object | Location of car engine (front, rear)	|	
| wheelbase | int64 | Weelbase of car |
| carlength	| float | Length of car |
| carwidth | float | Width of car |
| carheight	| float | height of car |		
| curbweight | int64 |	The weight of a car without occupants or baggage |
| enginetype || Type of engine (dohc, dohcv, l, ohc, ohcf, ohcv, rotor) |
| cylindernumber | object | Cylinder placed in the car (eight, five, four, six, three, twelve, two) |
| enginesize | int64 | Size of car |
| fuelsystem | object | Fuel system of car (1bbl, 2bbl, 4bbl, idi, mfi, mpfi, spdi, spfi)	|	
| boreratio | float | Boreratio of car |
| stroke | float | Stroke or volume inside the engine |
| compressionratio | float | Compression ratio of car	|	
| horsepower | int64 | Horsepower |
| peakrpm | int64 | car peak rpm |	
| citympg | int64 | Mileage in city |		
| highwaympg | int64 | Mileage on highway |		
| price(Dependent variable)	| int64 |	Price of car |		


# Analysis:

### Data Cleaning:
### Exploratory Data Analysis:

# Construct:

### Linear Regression Model:

### RMSE:
RMSE is the standard deviation of the residuals. So, RMSE gives us the standard deviation of the unexplained variance by the model. It can be calculated by taking square root of Mean Squared Error. RMSE is an absolute measure of fit. It gives us how spread the residuals are, given by the standard deviation of the residuals. The more concentrated the data is around the regression line, the lower the residuals and hence lower the standard deviation of residuals. It results in lower values of RMSE. So, lower values of RMSE indicate better fit of data.

### R2 Score:
R2 Score is another metric to evaluate performance of a regression model. It is also called coefficient of determination. It gives us an idea of goodness of fit for the linear regression models. It indicates the percentage of variance that is explained by the model.

Mathematically,

R2 Score = Explained Variation/Total Variation

In general, the higher the R2 Score value, the better the model fits the data. Usually, its value ranges from 0 to 1. So, we want its value to be as close to 1. Its value can become negative if our model is wrong.
### Hypothesis Testing:

# Execute:
### Summary of the analysis:

### Limitation of the project:

## List of Reference:

* [Automobile dataset](https://www.kaggle.com/datasets/fazilbtopal/auto85)
* [Drive Wheels](https://gomechanic.in/blog/drivetrains-explained/)
* [What is the difference between OHV, OHC, SOHC and DOHC engines?](https://www.samarins.com/glossary/dohc.html)
* [Pros and Cons of Turbo engines](https://www.samarins.com/check/turbo-car.html)
* [What is horsepower and why does it matter?](https://www.carwow.co.uk/guides/glossary/what-is-horsepower)
* [Why the Most Powerful Engines Have Short Strokes and Big Bores](https://www.roadandtrack.com/car-culture/a30443334/engine-stroke-vs-bore-explained/)
* [What is a car’s compression ratio?](https://www.torque.com.sg/features/what-is-a-cars-compression-ratio/)
* [Seaborn Scatterplot documentation](https://seaborn.pydata.org/generated/seaborn.scatterplot.html)
* [The Four Assumptions of Linear Regression](https://www.statology.org/linear-regression-assumptions/)
* [Simple Linear Regression in Machine Learning](https://www.javatpoint.com/simple-linear-regression-in-machine-learning)
