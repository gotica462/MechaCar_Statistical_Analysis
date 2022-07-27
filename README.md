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

## Summary Statistics on Suspension Coils

We used the MechaCar Suspension_Coil.csv dataset, in which  the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots, and created a summary statistics table using our knowledge of R.

See below for the results of the suspension coil’s PSI continuous variable across all manufacturing lots

![image](https://github.com/gotica462/MechaCar_Statistical_Analysis/blob/main/Total_Summary.png)

See below for the reslts for PSI metrics for each lot: mean, median, variance, and standard deviation.

![image](https://github.com/gotica462/MechaCar_Statistical_Analysis/blob/main/Lot_Summary.png)

- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

If we look at the total, then yes, the current manufacturing date meets the design specification requirement since the variance for all manufactoring lot is 62.9, which is less than 100. However is we look at each lot individually we find that only Lot 1 and Lot 2 meet the required specification. Lot 3 has a variance of more than 170 which exceeds the limit of 100 and fails the required design specification.

## T-Tests on Suspension Coils

Using your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

See results below for the t-test of all manufacturing lots

![image](https://github.com/gotica462/MechaCar_Statistical_Analysis/blob/main/Alllots.png)

The results shows that are P-Value (0.06) is > than our significance value. Therefore we do not have sufficient evidence to reject the null hypothesis. All manufacturing lots are statistically similar to the population mean of 1,500 pounds per square inch.

See rbelow for results for each lot individually.

Lot 1

![image](https://github.com/gotica462/MechaCar_Statistical_Analysis/blob/main/Lot1.png)

Lot 2

![image](https://github.com/gotica462/MechaCar_Statistical_Analysis/blob/main/Lot2.png)

Lot 3

![image](https://github.com/gotica462/MechaCar_Statistical_Analysis/blob/main/lot3.png)


In Lots 1 and 2  our p-values of 1 and 0.6 are greater than our significance value (0.05).  We do not have sufficient evidence to reject the null hypothesis, and we would state that lot1 and lot 2 are statistically similar to the population mean of 1,500 pounds per square inch. However our lot3 p-value (0.04) is less than our significance value (0.05) and in this case  we do have sufficient evidence to reject the null hypothesis, and we could say that lot3 is statistically different from the population mean of 1,500 pounds per square inch.


shows that p-value = 1 > 0.05 (significance value). That means we do not have sufficient evidence to reject the null hypothesis, and we would state that lot1 is statistically similar to the population mean of 1,500 pounds per square inch.

## Study Design: MechaCar vs Competition

Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

As a parent, one of my main concerns is safety, specifically I would like to Know if the MechaCar model is considered safer than other vehicles, so I would conduct a study to compare the metrics to see how often each manufacturer appear in accidents and see if the MechaCar appears more or less frequently than others.

I would start with the following hypothesis

Null hypothesis: There is no difference in frequency MechaCar accidents compared to competitors

Alternative hypothesis: There is difference in frequency MechaCar accidents compared to competitors

I would use a chi-squared test because i want to know if there is a difference in categorical frequencies between groups? (In our case vehicle's manufacturers) and I would like to compare it between groups.

The data set I would need to run would be one containing accident data in the US, I could go as far back as five years, and I would like to have categories of falta accidents and vehicle models. Maybe use the paige of the NHTSA (National Highway Traffic Safety Association) to get the information needed.





