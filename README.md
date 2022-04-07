# MechaCar Statistical Analysis

## Linear Regression to Predict MPG

The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. 

![pvalue deliverable 1](https://github.com/BPeaver/MechaCar_Statistical_Analysis/blob/main/Images/pvalue%20deliverable%201.png)

### Summary of Linear Regression Model
1: Looking at the above linear regression model, we can see that Vehicle Length and Ground Clearance are the only two variables that have significant effect on the MechaCar prototype's MPG rating. The remaining variables (Vehicle Weight, Spoiler Angle, and AWD) have random amounts of variance with the data.
2: The slope of this linear regression model is not zero, assuming a significance levle of 0.05%, due to our p-Value being 5.35e-11. This is sufficient to reject our null hypothesis.
3: Using our r-squared value of 0.7149, we can assume that approximately 71% of future MPG predicitions can be determined with this model. This means that this regression model predicts MechaCar prototype MPG relatively effectively. If we remove the other variables (Vehicle Weight, Spoiler Angle, and AWD), our r-squared value drops to 0.674, a minor reduction of 4% reliability (see below figure).

![eliminate insignificants deliverable 1](https://github.com/BPeaver/MechaCar_Statistical_Analysis/blob/main/Images/eliminate%20insignificants%20deliverable%201.png)


## Summary Statistics on Suspension Coils

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. In the Suspension_Coil.csv dataset, we have PSI information for three different lots of prototypes. Looking at a summary of all three lots' PSI values, we can see that the variance is approaching the 100 PSI limit set by the MechaCar design specifications. 

![total summary deliv 2](https://github.com/BPeaver/MechaCar_Statistical_Analysis/blob/main/Images/total%20summary%20deliv%202.png)

If we break it down into the three different prototype lots, we can see that Lot 3 is above the set threshhold at 170.2861224. 

![lot summary deliv 2](https://github.com/BPeaver/MechaCar_Statistical_Analysis/blob/main/Images/lot%20summary%20deliv%202.png)

While Lot 1 and Lot 2 contain some slight variance, they are both well within the stated specifications for the prototypes. This indicates there may be a problem with Lot 3's production methods. The below box plot provides a more visual and less numerical representation of the differences between Lots 3 compared to Lots 1 and 2.

![box plot lot sum deliv 2](https://github.com/BPeaver/MechaCar_Statistical_Analysis/blob/main/Images/box%20plot%20lot%20sum%20deliv%202.png)

## T-Tests on Suspension Coils

T-test summary across all prototype manufacturing lots testing PSI:

![one sample ttest deliv 3](https://github.com/BPeaver/MechaCar_Statistical_Analysis/blob/main/Images/one%20sample%20ttest%20deliv%203.png)

This t-test shows us that the true mean (also seen in the above total summary for all lots) is 1498.78 and  the p-Value is 0.06028. With this p-Value being higher than the standard significance level of 0.05, we can determine there is not enough evidence to reject the null hypothesis, i.e. the mean of all three lots is statistically similiar to the full population mean of 1500.

However, if we look at t-tests for each lot seperately:

![ttest for each lot deliv 3](https://github.com/BPeaver/MechaCar_Statistical_Analysis/blob/main/Images/ttest%20for%20each%20lot%20deliv%203.png)

We can see that Lot 1 and Lot 2 have means at or near 1500 PSI and p-Values that indicate we cannot reject a null hypothesis that there is no statistical difference between observed sample mean and presumed population mean. However, Lot 3 has issues, as mentioned in the prior section. The sample mean is less than 1500 and it's p-Value indicates we can reject the null hypothesis that sample mean and population mean are not statistically different. A closer look into the production of Lot 3 is required to find where these quality issues are originating in the process and remedy them. 

## Study Design: MechaCar vs Competition



