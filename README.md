# MechaCar_Statistical_Analysis

## Overview

To review thje production data for AutosRUs/ newest prototyp, the MechaCar, and give insights that may help the manufacturing team by doing statistical analysis like:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Linear Regression to Predict MPG

Using The MechaCar_mpg.csv dataset that contains mpg test results for 50 prototype MechaCars, and using R studio, we created a linear model that predicts the mpg of MechaCar prototypes using several variables such as vehicle lenght, vehicle weight, spoiler angle and ground clearance and AWD. 

See below for the results of our multiple linear model

![image](https://github.com/gotica462/MechaCar_Statistical_Analysis/blob/main/P-value%20and%20R_square%20value.png)

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

Based on our results, the varaibles ground clearance, vehicle length, and intercept provided a non-random amount of variance to the mpg values in the dataset since their p-value is less than 0.05. Therefore,they are statistically unlikely to provide random amounts of variance to the linear model. 

 -Is the slope of the linear model considered to be zero? Why or why not?
 
No, the slope of our lineal model is not zero. Because our p-value = 5.35 x 10*-11) which is much smaller than the significance level of 0.05. So there is enough evidence to reject or null hypothesis. 
            
- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

Yes, it does predcit the mpg of MechaCar prototypes effectively, because its r-value is greater than 0.7 (our it's 0.7149) and that indicates a strong correlation.

