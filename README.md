# Bike Sharing Case Study


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.


A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 


In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.


They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demands
Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors. 

 
## Business Objectives

You are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.

## Technologies Used
- numpy version	: 1.23.5
- pandas version	: 2.1.4
- seaborn version	: 0.13.2
- Python version	: 3.10.13

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Conclusions


#### - An optimal Linear regression model is built with the following predictor variables which decide the demand of the bike:

year, holiday, temp, windspeed, sep, sun, Light_snowrain, Misty, spring, summer and winter
           
#### - Equation of the best fitted model is:

 count = 0.1981 + 0.2340 * year + 0.4782 * temp - 0.1043 * holiday - 0.1480 * windspeed + 0.0894 * sep - 0.0495 * sun - 0.2904 * Light_snowrain - 0.0809 * Misty - 0.0544 * spring + 0.0623 * summer + 0.0969 * winter


#### -  Comparision between Training and Testing dataset:

Train dataset R^2 : 0.839

Test dataset R^2 : 0.8066

Train dataset Adjusted R^2 : 0.835

Test dataset Adjusted R^2 : 0.7963

#### - Following are the observation from the analysis

* Fall season seems to have attracted more booking. And, in each season the booking count has increased drastically from 2018 to 2019.
* Most of the bookings has been done during the month of may, june, july, aug, sep and oct. Trend increased starting of the year till mid of the year and then it
started decreasing as we approached the end of year.
* Clear weather attracted more booking which seems obvious.
* Thu, Fri and Sat have more number of bookings as compared to the start of the week.
* When it’s not holiday, booking seems to be less in number which seems reasonable as on holidays, people may want to spend time at home and enjoy with family.
* 2019 attracted more number of booking compared to the previous year, which shows good progress in terms of business.

#### 
Positive Indicators:
 * High R-squared value (0.839): This suggests that the model explains a significant portion of the variance in the dependent variable (count).
 * Means Square Error (MSE) values (0.00924) indicate model having good performance as it gives relatively low error.
 * Low p-values for most coefficients: These indicate that the corresponding features are statistically significant predictors of the target variable.
 * F-statistic with a low p-value (1.176e-185): This suggests that the overall model is statistically significant.
Areas for Further Investigation:
 * Durbin-Watson statistic (2.102): While this value is close to 2, indicating no significant autocorrelation, it might be worth investigating further to ensure the residuals are uncorrelated.
 * Jarque-Bera test: The p-value (163.903) suggests that the residuals are not normally distributed. This could affect the validity of the model's statistical inferences.
 * Condition number (17.3): This is relatively low, indicating that the features are not highly correlated, which is generally good. However, a very high condition number could signal multicollinearity.
Additional Considerations:
 * Model validation: The model's performance should be evaluated on a separate holdout dataset to assess its generalization ability.
 * Feature importance: Analyzing the absolute values of the standardized coefficients can provide insights into the relative importance of each feature in predicting the target variable.
 * Residual analysis: Plotting residuals against predicted values can help identify patterns or outliers that might indicate model misspecification.
To make a definitive judgment about the model's accuracy, it's recommended to:
 * Conduct a more comprehensive residual analysis.
 * Evaluate the model's performance on a holdout dataset.
 * Consider using other evaluation metrics, such as mean squared error (MSE) or root mean squared error (RMSE), in addition to R-squared.
By addressing these points, you can gain a more complete understanding of the model's accuracy and its suitability for the intended application.

## Contact
Created by @davisvarkey - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->