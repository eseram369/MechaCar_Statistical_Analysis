# MechaCar_Statistical_Analysis

# Deliverable 1
## Linear Regression to Predict MPG

### Resulting Model:
### mpg = (6.267)vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-104.0)

![ch15 del1](https://user-images.githubusercontent.com/90746609/148671440-ca832afd-a533-441f-b9f3-b78c007f7eb2.jpg)


### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
### The vehicle length and ground clearance are statistically viable to provide non-random amounts of variance to the model. the vehicle length and vehicle ground clearance significantly impact miles per gallon on the mechanical prototype. Conversely, the vehicle weight, spoiler angle, and All-Wheel Drive (AWD) have p-Values that indicate a random amount of variance with the dataset

### Is the slope of the linear model considered to be zero? Why or why not?
### The p-Value for this model, p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This means there is sufficient evidence to reject our null hypothesis, suggesting that this linear model's slope is not zero.

### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
This linear model has an r-squared value of 0.7149, which means that this model will determine approximately 71% of all mpg predictions. His multiple regression model does predict the mpg of MechaCar prototypes effectively.

# Deliverable 2:
## Summary Statistics on Suspension Coils

### The Suspension Coil dataset provided for the MechaCar contains testing the weight capacities of multiple suspension coils from multiple production lots to determine consistency.
### First looking at all manufacturing lots:


![ch15 del21](https://user-images.githubusercontent.com/90746609/148672005-b39d357a-5c6f-4dbc-b1ce-82b15c1c66ad.jpg)

### Diving a little deeper into each of the 3 lots:

![ch15del22](https://user-images.githubusercontent.com/90746609/148672023-5bbba478-e342-4ba2-b7f5-7f6d6739cacf.jpg)

### The MechaCar suspension coils' design specifications mandate that the suspension coils' variance cannot exceed 100 pounds per square inch (PSI) .

### Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
### When looking at the production lot's entire population, the coils' variance is 62.29 PSI, which is well within the 100 PSI variance requirement.
###Similarly, but significantly more consistent, Lot 1 and Lot 2 are well within the 100 PSI variance requirement, with 0.98 and 7.47, respectively. However, Lot 3 showed a much larger variance in performance and consistency, with a variance of 170.29. It is Lot 3 that is disproportionately causing the variance at the full lot level.
This very simple boxplot illustrates the differences between the lots:

![ch15del23](https://user-images.githubusercontent.com/90746609/148672335-d604c205-c315-42cb-a419-f3a59efcf8ef.jpg)


# DELIVERABLE 3

## t-Tests on Suspension Coils

### The next step is to conduct a t-test on the suspension coil data to determine whether there is a statistical difference between the mean of this provided sample dataset and a hypothesized potential population dataset. Using the presumed population mean of 1500, we find the following:
There is a summary of the t-test results across all manufacturing lots.
![ch15del31](https://user-images.githubusercontent.com/90746609/148672588-912646cc-48e0-4557-823c-cbc26a848fc0.jpg)

### From here, we can see the true mean of the sample is 1498.78, which we also saw in the summary statistics above. With a p-Value of 0.06, which is higher than the common significance level of 0.05, there is NOT enough evidence to support rejecting the null hypothesis. That is to say, the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 1500.
Next looking at each lots:
### Lot 1 sample has the true sample mean of 1500, again as we saw in the summary statistics above. With a p-Value of 1, we cannot reject (i.e. accept) the null hypothesis that there is no statistical difference between the observed sample mean and the presumed population mean (1500).
### Lot 2 has essentially the same outcome with a sample mean of 1500.02, a p-Value of 0.61; the null hypothesis cannot be rejected. The sample mean and the population mean of 1500 are statistically similar.
However, Lot 3, not surprisingly, is a different scenario. Here the sample mean is 1496.14 and the p-Value is 0.04, which is lower than the standard significance level of 0.05. All indicate to reject the null hypothesis that this sample mean and the presumed population mean are not statistically different.
How does this information help? Clearly, something went awry in Lot 3's production cycle. The process needs to be checked for system fails and the suspension coils from this lot need to be inspected to remove those not meeting quality criteria.

![ch15del32](https://user-images.githubusercontent.com/90746609/148672667-9f57be01-ffba-4870-884c-0bb0854d630e.jpg)



# Deliverable 4:
## Study Design: MechaCar vs Competition
### Using your knowledge of R, design a statistical study to compare the performance of the MechaCar vehicles against the performance of vehicles from other manufacturers.
### The statistical study design has the following:
- A metric to be tested is mentioned
- A null hypothesis or an alternative hypothesis is described
- A statistical test is described to test the hypothesis
### This study would involve collecting data on MechaCar and its comparable models across several different manufacturers over the last 3 years.
- What metric or metrics are you going to test?
### Metrics
### Collecting data for comparable models across all major manufacturers for the past 3 years for the following metrics:
- Safety Feature Rating: Independent Variable
- Current Price (Selling): Dependent Variable
- Drive Package : Independent Variable
- Engine (Electric, Hybrid, Gasoline / Conventional): Independent Variable
- Resale Value: Independent Variable
- Average Annual Cost of ownership (Maintenance): Independent Variable
- MPG (Gasoline Efficiency): Independent Variable

- What is the null hypothesis or alternative hypothesis?
### Hypothesis: Null and Alternative
### After determining which factors are key for the MechaCar's genre:

### Null Hypothesis (Ho): MechaCar is priced correctly based on its performance of key factors for its genre.
### Alternative Hypothesis (Ha): MechaCar is NOT priced correctly based on performance of key factors for its genre.

- What statistical test would you use to test the hypothesis? And why?
### Statistical Tests
###A multiple linear regression would be used to determine the factors that have the highest correlation/predictability with the list selling price (dependent variable); which combination has the greatest impact on price (it may be all of them!)



- What data is needed to run the statistical test?
### Sample A: sufficiently large MecharCar sample data set of fuel efficiency
### Sample B: sufficiently large competition sample data set of fuel efficiency



