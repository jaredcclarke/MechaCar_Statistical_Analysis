# MechaCar_Statistical_Analysis
## Overview 
### Purpose
The purpose of this exercise is to use R and statistical analysis of AutosRus' production data to give the manufacturing team insights to help alleviate their produciton troubles with their new car, the MechaCar.

### Resources/Tools
* R version 4.0.3
* R Studio version 1.4.1103
* MechaCar_mpg.csv
* Suspension_Coil.csv
* R dplyr library

## Linear Regression to Predict MPG
### Deliverable 1 
![](https://github.com/jaredcclarke/MechaCar_Statistical_Analysis/blob/main/Resources/lm_summary.png)

* Looking at this linear regression data, vehicle length and ground clearance provided non-random amount of variance in the dataset because their `Pr(>|t|)` values were significantly lower than (2.06e-12 & 5.21e-88, respectively) the significance level of .05.
* With the p-value being 5.35e-11, it is lower than the significance level of .05, and therefore the null hypothesis of the slope being zero can be rejected.
* This linear regression model has an R squared value of 0.7149 so that means this model can predict the mpg of the MechaCar 71% of the time

## Summary Statistics on Suspension Coils
### Deliverable 2
`Table 1`

![](https://github.com/jaredcclarke/MechaCar_Statistical_Analysis/blob/main/Resources/Total_Summary.png)

`Table 2`

![](https://github.com/jaredcclarke/MechaCar_Statistical_Analysis/blob/main/Resources/lot_summary.png)

* The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 psi.
* Created a table to show the suspension coil’s PSI continuous variable across all manufacturing lots (Table 1)
* The following PSI metrics for each lot: mean, median, variance, and standard deviation. (Table 2)
* The total suspension coil variance for all three lots is under 100 psi, meeting the requirement, but when looking at lot 3, it does not meet the design requirement due to the variance being 170.286 

## T-Tests on Suspension Coils
### Deliverable 3
* Performed t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

`All Lots`

![](https://github.com/jaredcclarke/MechaCar_Statistical_Analysis/blob/main/Resources/all_lots_ttest.png)

* P-value = 0.06028, which is greater than the signifinace value of .05, therefore we do not have enough evidence to reject the null hypothesis, meaning that all lots are not statistically different from the population mean of 1,500 psi.

`Lot 1`
![](https://github.com/jaredcclarke/MechaCar_Statistical_Analysis/blob/main/Resources/Lot1.png)

* P-value = 1, which is greater than the signifinace value of .05, therefore we do not have enough evidence to reject the null hypothesis, meaning that all lots are not statistically different from the population mean of 1,500 psi.

`Lot 2`
![](https://github.com/jaredcclarke/MechaCar_Statistical_Analysis/blob/main/Resources/Lot2.png)

* P-value = 0.06072, which is greater than the signifinace value of .05, therefore we do not have enough evidence to reject the null hypothesis, meaning that all lots are not statistically different from the population mean of 1,500 psi.

`Lot 3`
![](https://github.com/jaredcclarke/MechaCar_Statistical_Analysis/blob/main/Resources/lot3.png)

* P-value = 0.04168, which is very close to the significance value of .05, therefore we do not have enough evidence to reject the null hypothesis, meaning that all lots are not statistically different from the population mean of 1,500 psi.

## Study Design: MechaCar vs Competition
### Description
A statistical study that can compare MechaCar and their carbon dioxide emissions compared to other companies

### Metrics
* Horsepower
* Vehicle Weight
* Carbon dioxide emissions
* Fuel efficiency
* MPG

### Huypotheses
* Null Hypothesis - MechaCar has the same or more carbon dioxide emissions than the competition
* Alternative Hypothesis - MechaCar has less carbon dioxide emissions than the competition

### Statistical Tests
* Multiple linear regression to see if the metrics had a relationship with carbon dioxide emissions
* ANOVA test to test the difference in the variance of the means of MechaCar and the competition

### Data
* Data needed for this experiment are the metrics listed above from both MechaCar and the competion.
