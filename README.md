# Predicting Car Prices
## Linear Regression and Hypothesis Testing use case

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
