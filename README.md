# Predicting Car Prices
## By Building Simple and Multiple Linear Regression Models

# Introduction:

Linear Regression is a technique that estimates the linear relationship between a continuous dependent variable and one or more independent variables.This technique is applicable for Supervised learning Regression problems where we try to predict a continuous variable.

Linear Regression can be classified into two types –

1. **Simple Linear Regression**: Simple Linear Regression is a type of regression algorithms that models the relationship between a dependent variable and a single independent variable.

2. **Multiple Linear Regression**: Multiple Linear Regression is a type of regression algorithms that models the linear relationship between a single dependent continuous variable and more than one independent variable.


## 1. Linear Regression Model:

Simple Linear Regression (or SLR) is the simplest model in machine learning. It models the linear relationship between the independent and dependent variables.

<img align="center" src="https://static.javatpoint.com/tutorial/machine-learning/images/linear-regression-in-machine-learning.png">

In this project, the independent/predictor variable is car engine size data and is denoted by X. Similarly, the dependent/response variable represents the Car price data and is denoted by y. We want to build a linear relationship between these variables.

This linear relationship can be modelled by mathematical equation of the form:-

Y = β0 + β1 * X

where:
* Y: The response variable
* X: The jth predictor variable
* β0(Intercept): The value of Y when X = 0
* β1(Slope): The average effect on Y of a one unit increase in Xj, holding all other predictors fixed
 
β0 and β1 are called parameters of the model.

In this Simple Linear Regression model, we want to fit a line which estimates the linear relationship between X and Y. The values for β0 and β1 are chosen using the Ordinary Least Square (OLS) method, which minimizes the sum of squared residuals (RSS).

RSS = Σ(yi – ŷi)2      where, yi = actual value and  ŷi = predicted value

## Assumptions of Simple Linear Regression Model:

1. **Linear relationship**: There exists a linear relationship between the independent variable, x, and the dependent variable, y.
2. **Independence**: The residuals are independent. In particular, there is no correlation between consecutive residuals in time series data.
3. **Homoscedasticity**: The residuals have constant variance at every level of x.
4. **Normality**: The residuals of the model are normally distributed.

## 2. Multiple Linear Regression Model 

Multiple Linear Regression is one of the important regression algorithms which models the linear relationship between a single dependent continuous variable and more than one independent variable.

For MLR, the dependent or target variable(Y) must be the continuous/real, but the predictor or independent variable may be of continuous or categorical form.

Y = β0 + β1X1 + β2X2 + … + βpXp + ε

where:
* Y: The response variable
* Xj: The jth predictor variable
* βj: The average effect on Y of a one unit increase in Xj, holding all other predictors fixed
* ε: The error term

The values for β0, β1, B2, … , βp are chosen using the least square method, which minimizes the sum of squared residuals (RSS).

RSS = Σ(yi – ŷi)2

## Assumptions of Multiple Linear Regression Model:

1. **Linear relationship**: There exists a linear relationship between each predictor variable and the response variable.
2. **No Multicollinearity**: None of the predictor variables are highly correlated with each other.
3. **Independence**: The observations are independent.
4. **Homoscedasticity**: The residuals have constant variance at every point in the linear model.
5. **Multivariate Normality**: The residuals of the model are normally distributed.

## Goal of the project:
In this project -

* We'll find out if there is any correlation between car's price and engine size.
* Create a simple and a multiple linear regression model to predict car's price based on other variables.
* Find the equation of the regression (best fit) line.
* Evaluate the performance of these models.

## About the dataset: 
The [dataset](https://doi.org/10.24432/C5B01C) contains 205 instances(rows) with 26 features of car models from 1985 Ward's Automotive Yearbook and is distributed by UCI Machine Learning Repository.

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

* Reliability: The data is distributed by UCI Machine Learning Repository. So it is reliable to use.
* Comprehensiveness: The dataset contains the required data for our project purpose. Thus it is comprehensive.
* Citation: Schlimmer,Jeffrey. (1987). Automobile. UCI Machine Learning Repository. https://doi.org/10.24432/C5B01C.
* Current: The data was donated on 5/18/1987. Clearly it is an outdated data.

# Analysis: 
### Data Cleaning:

The initial data cleaning is done in Excel.
* Checked for duplicate entries.
* Changed the column headers to lower case.
* Corrected the typos and misspellings.
* Formatted the variables correctly.

### Exploratory Data Analysis:

* Checked the shape and general information of the dataset and dropped the unnecessary columns.
* The dataset contain several missing values and outliers. In order to build the regression model, we've eliminated them.
* Performed descriptive statistcis.
* Plotted the distribution of the numerical variables in order to check whether they're normally distributed or not.

  ![dist](https://github.com/Arpita-deb/Car-Price-Prediction/assets/139372731/96a2cbff-0de5-4330-8b32-7a45f7ccb56d)

* Plotted countplot (bar charts) to see the distribution of categorical variables.
* Plotted Heatmap and correlation matrix to find the correlation strength of the variables.

  ![heatmap](https://github.com/Arpita-deb/Car-Price-Prediction/assets/139372731/07b10b97-4dfd-49a0-8da3-d6f25889484a)

* Identified the dependent/response and independent/feature variables for the models.
  * For Simple Linear Regression Model: dependent/response variable : *price*, independent/feature variables : *engine size*
  * For Multiple Linear Regression Model: dependent/feature variable : *price*, independent/feature variables : *length, width, curb_weight, engine_size, horsepower, highway_mpg*                             
* Plotted pairplot to check linearity and normality of the feature variables.

![pairplot](https://github.com/Arpita-deb/Car-Price-Prediction/assets/139372731/9278219d-4980-4395-b9ba-3e19c9e6dc18)

* Created two different datasets for simple and multiple linear models.

# Model Construct:

## Steps to build Linear Regression Models:
The following steps are taken for both the models.

1. Import the required packages, functions, and classes
2. Load data to work with and, if appropriate, transform it
3. Create a classification model and train (or fit) it with existing data
4. Predicting the test result
5. Testing the performance of the model by calculating evaluation matrices.

## 1. Simple Linear Regression Model:

The equation for best fit line for a simple linear regression model is expressed as - 
**price** = - 8294.23 + 167.04 * **engine_size**

It means one unit increase in engine size will increase 167.04 unit in price of a car. The regression line for the test data is shown here - 

![reg line slr](https://github.com/Arpita-deb/Car-Price-Prediction/assets/139372731/276af15f-7b29-499b-aa6e-5e7079d75efb)

The difference between the observed value of the dependent variable (yi) and the predicted value (ŷi) is called the residual and is denoted by e. The scatter-plot of these residuals is called residual plot.
e = yi - ŷi
If the data points in a residual plot are randomly dispersed around horizontal axis and an approximate zero residual mean, a linear regression model may be appropriate for the data. Otherwise a multiple or polynomial regression model might be a better fit. 

This scatterplot gives us whether or not this model met the Homoscedasticity Assumption. If we take a look at the generated ‘Residual errors’ plot, we can clearly see that the train data plot pattern is non-random. Same is the case with the test data plot pattern. So, it suggests a better-fit for a non-linear model.

![cloud slr](https://github.com/Arpita-deb/Car-Price-Prediction/assets/139372731/31321769-c3f9-4a96-a312-0c13e62221f1)

And this histogram gives us whether or not this model met the Normality Assumption. Since the residuals are normally distributed, it has met the normality condition.

![resid slr](https://github.com/Arpita-deb/Car-Price-Prediction/assets/139372731/c49279c3-8114-4425-a6bd-dd35a4b7a9a4)

## 2. Multiple Linear Regression Model:

The equation for best fit line for a Multiple linear regression model is expressed as - 

**price** = -18583.60 + 54.34 * **length** + 19.05 * **width** + 5.89 * **curb_weight** - 1.67 * **engine_size** + 47.29 * **horsepower** + 3.21 * **highway_mpg**

The scatterplot of residuals are more random than the simple linear regression model. There are no clear pattern in this chart. So we can say it met the Homoscedasticity condition.

![cloud mlr](https://github.com/Arpita-deb/Car-Price-Prediction/assets/139372731/842e7eee-faaf-4faa-ad8b-ef84f64cbc46)

The residuals are normally ditributed but there are some large values of residuals which mean that some of the model's predictions were quite off the mark.

![resid mlr](https://github.com/Arpita-deb/Car-Price-Prediction/assets/139372731/78636957-c5fe-4587-921c-1342c92b78cf)

# Execute:

## Evaluation Matrix:

1. **RMSE**: RMSE is the standard deviation of the residuals. So, RMSE gives us the standard deviation of the unexplained variance by the model. It can be calculated by taking square root of Mean Squared Error.

    RMSE is an absolute measure of fit. It gives us how spread the residuals are, given by the standard deviation of the residuals. The more concentrated the data is around the regression line, the lower the residuals and hence lower the standard deviation of residuals. It results in lower values of RMSE. So, lower values of RMSE indicate better fit of data.

2. **R2 Score**: R2 Score is another metric to evaluate performance of a regression model. It is also called coefficient of determination. It gives us an idea of goodness of fit for the linear regression models. It indicates the percentage of variance that is explained by the model.

     The value for R-squared can range from 0 to 1. A value of 0 indicates that the response variable cannot be explained by the predictor variable at all. A value of 1 indicates that the response variable can be perfectly explained without error by the predictor variable.

3. **Training set score**: It quantifies the number of correct predictions of the model on the training dataset. The higher the score the better the model performed on the training dataset.

4. **Test set score**: It quantifies the number of correct predictions of the model on the testing dataset. The higher the score the better the model performed on the testing dataset.

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
* [StatQuest - Linear Regression Clearly Explained](https://youtu.be/7ArmBVF2dCs?si=HEyYKuT4uqtXTbNh)
* [Seaborn Scatterplot documentation](https://seaborn.pydata.org/generated/seaborn.scatterplot.html)
* [The Four Assumptions of Linear Regression](https://www.statology.org/linear-regression-assumptions/)
* [Simple Linear Regression in Machine Learning](https://www.javatpoint.com/simple-linear-regression-in-machine-learning)
* [Introduction to Multiple Linear Regression](https://www.statology.org/multiple-linear-regression/)
