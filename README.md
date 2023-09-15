# Predicting Car Prices

Linear Regression is a technique that estimates the linear relationship between a continuous dependent variable and one or more independent variables.This technique is applicable for Supervised learning Regression problems where we try to predict a continuous variable.

Linear Regression can be classified into two types –

1. **Simple Linear Regression**: Simple Linear Regression is a type of Regression algorithms that models the relationship between a dependent variable and a single independent variable.

2. **Multiple Linear Regression**: Multiple Linear Regression is one of the important regression algorithms which models the linear relationship between a single dependent continuous variable and more than one independent variable.

## Goal of the project:
In this project -

* We'll find out if there is any correlation between car's price and engine size two variables.
* Create a simple and a multiple linear regression model to predict car's price based on other variables.
* Find the equation of the regression (best fit) line.
* Evaluate the performances of these models and choose the one with higher score.

## About the dataset: 
The dataset contains 205 instances(rows) with 26 features of car models from 1985 Ward's Automotive Yearbook.

### Data Dictionary:
| Column Name | Data Type | Column Description |
| :--- | :--- | :--- |	
| symboling | int64 |	Its assigned insurance risk rating, A value of +3 indicates that the auto is risky, -3 that it is probably pretty safe |	
| normalized_losses | float | normalized losses for each car |
| car_company | object | Name of car company |
| fuel_type | object | Car fuel type i.e gas or diesel |
| aspiration | object | Aspiration used in a car |
| no_of_doors | object | Number of doors in a car |	
| body_style | object |	Body of car (hardtop, wagon, sedan, hatchback, convertible) |
| drive_wheels | object | Type of drive wheel (4wd, fwd, rwd) |	
| engine_location | object | Location of car engine (front, rear)	|	
| wheel_base | int64 | Weelbase of car |
| length	| float | Length of car |
| width | float | Width of car |
| height	| float | height of car |		
| curb_weight | int64 |	The weight of a car without occupants or baggage |
| engine_type | object | Type of engine (dohc, dohcv, l, ohc, ohcf, ohcv, rotor) |
| no_of_cylinders | object | Cylinder placed in the car (eight, five, four, six, three, twelve, two) |
| engine_size | int64 | Size of car |
| fuel_system | object | Fuel system of car (1bbl, 2bbl, 4bbl, idi, mfi, mpfi, spdi, spfi)	|	
| bore | float | Boreratio of car |
| stroke | float | Stroke or volume inside the engine |
| compression_ratio | float | Compression ratio of car	|	
| horsepower | int64 | Horsepower |
| peak_rpm | int64 | car peak rpm |	
| city_mpg | int64 | Mileage in city |		
| highway_mpg | int64 | Mileage on highway |		
| price	| int64 |	Price of car |		

### Data Integrity and Validation:

* Reliability:
* Originality:
* Comprehensiveness:
* Citation:
* Current:

# Analysis:

### Data Cleaning:

The initial data cleaning is done in Excel.
* 

### Exploratory Data Analysis:



# Model Construct:

## 1. Linear Regression Model:

Simple Linear Regression (or SLR) is the simplest model in machine learning. It models the linear relationship between the independent and dependent variables.

![SLR](https://static.javatpoint.com/tutorial/machine-learning/images/linear-regression-in-machine-learning.png)

In this project, the independent/predictor variable is car engine size data and is denoted by X. Similarly, the dependent/response variable represents the Car price data and is denoted by y. We want to build a linear relationship between these variables.

This linear relationship can be modelled by mathematical equation of the form:-

             Y = β0   + β1*X    -------------   (1)

β1 is the coefficient for independent variable (slope) and β0 is the intercept term. β0 and β1 are called parameters of the model.

In this Simple Linear Regression model, we want to fit a line which estimates the linear relationship between X and Y. So, the question of fitting reduces to estimating the parameters of the model β0 and β1.

**Ordinary Least Square Method** : Ordinary least squares estimates the beta coefficients in a linear regression model by minimizing a measure of error called the sum of squared residuals.
We can define an error function for any line. Then, the regression line is the one which minimizes the error function. Such an error function is also called a Loss function.

**Loss function** : A function that measures the distance between observed  values and the model’s estimated values.

We want the Regression line to resemble the dataset as closely as possible. In other words, we want the line to be as close to actual data points as possible. It can be achieved by minimizing the vertical distance between the actual data point and fitted line. This distance is called the residual.

![Lf](https://th.bing.com/th/id/R.880549d05c57fe96ababcb9ed4d9dd50?rik=YPuUc37DFkJSUQ&riu=http%3a%2f%2fwww.sthda.com%2fenglish%2fsthda-upload%2fimages%2fmachine-learning-essentials%2flinear-regression.png&ehk=svAm3xChWZwytrdGETUS%2fRhwtmbJuBtgZYcEOu3RkVQ%3d&risl=&pid=ImgRaw&r=0)

So, in a regression model, we try to minimize the residuals by finding the line of best fit. 

We can try to minimize the sum of the residuals, but then a large positive residual would cancel out a large negative residual. For this reason, we minimize the sum of the squares of the residuals.

Mathematically, we denote actual data points by yi and predicted data points by ŷi. So, the residual for a data point i would be given as di = yi - ŷi

**Cost function** : It denotes the total error present in the model which is the sum of the total errors of each individual data point.

We can estimate the parameters of the model β0 and β1 by minimizing the error in the model by minimizing D. Thus, we can find the regression line given by equation (1). This method of finding the parameters of the model and thus regression line is called Ordinary Least Square Method.

## Assumptions of Simple Linear Regression Model:

1. **Linear relationship**: There exists a linear relationship between the independent variable, x, and the dependent variable, y.

2. **Independence**: The residuals are independent. In particular, there is no correlation between consecutive residuals in time series data.

3. **Homoscedasticity**: The residuals have constant variance at every level of x.

4. **Normality**: The residuals of the model are normally distributed.

From the model output, the coefficients allow us to form an estimated simple linear regression model:
**price** = - 8294.23 + 167.04 * **engine_size**

## 2. Multiple Linear Regression Model 

Multiple Linear Regression is one of the important regression algorithms which models the linear relationship between a single dependent continuous variable and more than one independent variable.

For MLR, the dependent or target variable(Y) must be the continuous/real, but the predictor or independent variable may be of continuous or categorical form.

Y = β0 + β1X1 + β2X2 + … + βpXp + ε

where:

Y: The response variable
Xj: The jth predictor variable
βj: The average effect on Y of a one unit increase in Xj, holding all other predictors fixed
ε: The error term

The values for β0, β1, B2, … , βp are chosen using the least square method, which minimizes the sum of squared residuals (RSS):

RSS = Σ(yi – ŷi)2

From the model output, the coefficients allow us to form an estimated multiple linear regression model:

**price** = -18583.60 + 54.34 * **length** + 19.05 * **width** + 5.89 * **curb_weight** - 1.67 * **engine_size** + 47.29 * **horsepower** + 3.21 * **highway_mpg**

## Assumptions of Multiple Linear Regression Model:

1. **Linear relationship**: There exists a linear relationship between each predictor variable and the response variable.
   
2. **No Multicollinearity**: None of the predictor variables are highly correlated with each other. 

3. **Independence**: The observations are independent. 

4. **Homoscedasticity**: The residuals have constant variance at every point in the linear model.

5. **Multivariate Normality**: The residuals of the model are normally distributed.

# Execute:

## Evaluation Matrix:
1. **RMSE**: RMSE is the standard deviation of the residuals. So, RMSE gives us the standard deviation of the unexplained variance by the model. It can be calculated by taking square root of Mean Squared Error. RMSE is an absolute measure of fit. It gives us how spread the residuals are, given by the standard deviation of the residuals. The more concentrated the data is around the regression line, the lower the residuals and hence lower the standard deviation of residuals. It results in lower values of RMSE. So, lower values of RMSE indicate better fit of data.

2. **R2 Score**: R2 Score is another metric to evaluate performance of a regression model. It is also called coefficient of determination. It gives us an idea of goodness of fit for the linear regression models. It indicates the percentage of variance that is explained by the model.
This is often written as r2, and is also known as the coefficient of determination. It is the proportion of the variance in the response variable that can be explained by the predictor variable.

The value for R-squared can range from 0 to 1. A value of 0 indicates that the response variable cannot be explained by the predictor variable at all. A value of 1 indicates that the response variable can be perfectly explained without error by the predictor variable.

Mathematically,

R2 Score = Explained Variation/Total Variation

In general, the higher the R2 Score value, the better the model fits the data. Usually, its value ranges from 0 to 1. So, we want its value to be as close to 1. Its value can become negative if our model is wrong.

## Model Statistics: 


| Matrices | Simple Linear Regression | Multiple Linear Regression |
| :-- | :--- | :--- |
| Regression line equation | **price** = - 8294.23 + 167.04 * **engine_size** | **price** = -18583.60 + 54.34 * **length** + 19.05 * **width** + 5.89 * **curb_weight** - 1.67 * **engine_size** + 47.29 * **horsepower** + 3.21 * **highway_mpg** |
| β0 | - 8294.23 | -18583.60 |
| β1 | 167.04 | [ 54.34, 19.05, 5.89, -1.67, 47.29, 3.21 ] |
| Mean Squared Error (MSE) | 12932302.0331 | 5637566.7982 |
| Root Mean Squared Error (RMSE) | 3596.1510 | 3596.1510 |
| R-squared | 0.4600 | 0.7561 |
| Training set score | 0.6968 | 0.7929 |
| Test set score | 0.4600 | 0.7561 |

## Conclusion: 

Among these two models, clearly **Multiple Linear Regression model performs better than a simple Linear regression model** in correctly predicting the price of cars based on other variables. The Multiple Linear Regression model correctly predicted 75.61% of the test data while the Simple Linear Regression model could only predict 46% of the test data.

## Limitation of the project:
These models aren't perfect. There are certain limitations of these models.
1. The dataset is very small. It couldn't be split into train, test as well as validation set.
2. The data is clearly outdated which reduces its usability.
3. The distribution of price column is not normal. It is right skewed.
4. The homoscedasticity assumption for both the models didn't purely satisfy. 
5. There might be some multicollinearity among the feature variables (e.g. car width, length and curb weight).
6. In the multiple linear model only numerical columns are taken into account.  Some categorical variables (e.g. aspiration, fuel system, engine type etc) can also influence the price of a car.
7. Moreover, When using a regression equation to predict something we can only use values for the predictor variable that are within the range of the predictor variable in the original dataset we used to generate the least squares regression line. This means any values outside the dataset, will not product correct prediction.

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
* [Introduction to Multiple Linear Regression](https://www.statology.org/multiple-linear-regression/)
* [Simple Linear Regression in Machine Learning](https://www.javatpoint.com/simple-linear-regression-in-machine-learning)
