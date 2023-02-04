
# YULU - Hypothesis Testing

Yulu is India’s leading micro-mobility service provider, which offers unique vehicles for the daily commute. Starting off as a mission to eliminate traffic congestion in India, Yulu provides the safest commute solution through a user-friendly mobile app to enable shared, solo and sustainable commuting.

Yulu zones are located at all the appropriate locations (including metro stations, bus stands, office spaces, residential areas, corporate offices, etc) to make those first and last miles smooth, affordable, and convenient!

Yulu has recently suffered considerable dips in its revenues. They have contracted a consulting company to understand the factors on which the demand for these shared electric cycles depends. Specifically, they want to understand the factors affecting the demand for these shared electric cycles in the Indian market.

#### Business Problem

- The company wants to understand and process the data coming out of data engineering pipelines:

  >• Which variables are significant in predicting the demand for shared electric cycles in the Indian market?
  >• How well those variables describe the electric cycle demands

#### Dataset

The company collected the transactional data of customers. The dataset has the following features:
Dataset link: (https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/428/original/bike_sharing.csv?1642089089)

#### Column Profiling

*   datetime: datetime
*   season: season (1: spring, 2: summer, 3: fall, 4: winter)
*   holiday: whether day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
*   workingday: if day is neither weekend nor holiday is 1, otherwise is 0.
weather:
    1: Clear, Few clouds, partly cloudy, partly cloudy
    2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
    3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
    4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
*   temp: temperature in Celsius
*   atemp: feeling temperature in Celsius
*   humidity: humidity
*   windspeed: wind speed
*   casual: count of casual users
*   registered: count of registered users
*   count: count of total rental bikes including both casual and registered

#### Problem Scenarios

Concept Used:

*   Bi-Variate Analysis
*   2-sample t-test: testing for difference across populations
*   ANNOVA
*   Chi-square

- Visual analysis 
- Hypothesis formulation 
- Select the appropriate test 
- Check test assumptions 
- Find the p-value
- Conclusion based on the p-value 

#### Inferences and Recommendations

**Insights and Observations**

Insights

    > - In the summer and fall seasons, more bikes are rented as compared to other seasons.
    > - Whenever it's a holiday more bikes are rented.
    > - It is also clear from the working day also that whenever a day is a holiday or weekend, slightly more bikes were rented.
    > - Whenever there is rain, thunderstorm, snow, or fog, there were fewer bikes were rented.
    > - Whenever the humidity is less than 20, the number of bikes rented is sparse.
    > - Whenever the temperature is less than 10, the number of bikes rented is less.
    > - Whenever the windspeed is greater than 35, the number of bikes rented is less.

Univariate analysis

    > - The number of riders in all seasons is almost the same.
    > - More riders (97% of them) ride on non-holidays.
    > - More riders (68% of them) ride on working days.
    > - Nearly 92% of the riders ride on days when the weather is clear or partly clear.
    > - The mean and median temperature in the dataset is approximately around 20Â°C.
    > - The mean and the median feeling temperature in the dataset is approximately around 24Â°C.
    > - The mean and median humidity in the dataset is approximately around 62%.
    > - The windspeed is approximately around 13, with a large number of outliers.
    > - There is a large number of outliers for the casual, registered, and total count of riders between 1st Jan 2011 to 19th Dec 2012. That could be due to the increase in the number of riders over this period.

Bivariate analysis

    > - The number of casual, registered, and total riders increased considerably between 1st Jan 2011 to 19th Dec 2012.
    > - There is also a definite trend and seasonality as we can see an increase in the number of riders from spring to summer to fall and then a decrease in the number of riders in winter before rising again in spring next season.
    > - The median number of casual, registered, and total riders are highest in the fall and summer season followed by the winter and spring season.
    > - The median number of casual, registered, and total riders are almost equal irrespective of whether it is a holiday or not.
    > - The median number of casual, registered, and total riders are almost equal irrespective of whether it is a working day or not.
    > - The median number of casual, registered, and total riders are almost equal irrespective of whether it is a working day or not.
    > - The number of riders in every season is highest in clear and partly_clear weather

Correlation

    > - There is very less correlation between {temperature, feeling temperature, humidity and windspeed} and {casual, registered, and count} variables.
    > - There is a very strong correlation between temperature and feeling temperature.
    > - There is a very strong correlation between casual and total riders, as casual riders contribute to the total number of riders for Yulu.
    > - There is a very strong correlation between registered and total riders, as registered riders contribute to the total number of riders for Yulu.

General insights based on Statistical test

    > - The average number of cycles rented during working days and off days are significantly similar.
    > - Weather and seasons are dependent.
    > - Weather and temperature, Weather and humidity level are also dependent .
    > - There's a significant difference in demand during different weather and seasons.
    > -     o   The test statistic for temp is 0.9806709885597229 with p_value 9.445639856639374e-34 Hence at a 95% confidence level, we reject the null hypothesis Hence we can say that temp is not coming from a normally distributed population
    > -     o   The test statistic for atemp is 0.9834496974945068 with p_value 1.3297287311544133e-31 Hence at a 95% confidence level, we reject the null hypothesis Hence we can say that atemp is not coming from a normally distributed population
    > -     o   The test statistic for humidity is 0.9798952341079712 with p_value 2.6224124135481048e-34 Hence at a 95% confidence level, we reject the null hypothesis Hence we can say that humidity is not coming from a normally distributed population
    > -     o   The test statistic for windspeed is 0.9652013182640076 with p_value 1.4531465075048353e-42 Hence at a 95% confidence level, we reject the null hypothesis Hence we can say that windspeed is not coming from a normally distributed population
    > -     o   The test statistic for casual is 0.818075954914093 with p_value 0.0 Hence at a 95% confidence level, we reject the null hypothesis Hence we can say that casual is not coming from a normally distributed population
    > -     o   The test statistic for registered is 0.9053951501846313 with p_value 0.0 Hence at a 95% confidence level, we reject the null hypothesis Hence we can say that the registered is not coming from a normally distributed population
    > -     o   The test statistic for count is 0.9148815274238586 with p_value 0.0 Hence at a 95% confidence level, we reject the null hypothesis Hence we can say that count is not coming from a normally distributed population

Recommendations 

    - In the summer and fall seasons, the company should have more bikes in stock to be rented. Because the demand in these seasons is higher as compared to other seasons. 
    - With a significance level of 0.05, the working day has no effect on the number of bikes being rented.
    - On very low humid days, the company should have less bikes in stock to be rented.
    - Whenever the temperature is less than 10 or in very cold days, the company should have fewer bikes.
    - Whenever the windspeed is greater than 35 or in thunderstorms, the company should have fewer bikes in stock to be rented.
    - From the 2 Sample T-test, we have seen that a holiday has no impact on the number of riders at a 95% confidence level, Yulu should run similar promotional campaigns/offers irrespective of whether it is a holiday or not.
    - From the 2 Sample T-tests we have seen that a working day has no impact on the number of riders at a 95% confidence level, Yulu should run similar promotional campaigns/offers irrespective of whether it is a working day or not.
    - As we have seen from the Analysis of Variance(ANOVA), the mean number of riders is statistically different at a 95% confidence level for different seasons, Yulu should have different strategies for different seasons. Yulu should try to increase the number of riders in the months of fall and winter when the number of riders goes down considerably and maximize capacity utilization of e-bikes in the months of summer and fall.
    - As we have seen from the Analysis of Variance(ANOVA), the mean number of riders is statistically different at a 95% confidence level for different weathers, Yulu should have different strategies for different weathers. Yulu should try to maximize the capacity utilization of e-bikes when the weather is clear or partly clear.
    - As we have seen from Chi-Square Test that weather is dependent on seasons at a 95% confidence level. Yulu should maximize the capacity utilization or rides in every season when the weather is clear or partly_clear.
    - Yulu should perform demand forecasting as we have seen that there is a trend and seasonality in the data. Better demand forecasting will lead to better capacity utilization of e-bikes in different seasons.
    - Yulu should also perform a further investigation into the riders based on gender and age as insights into age bracket and gender would reveal a lot about the week-on-week capacity utilization on the type of customers preferring Yulu e-bikes.

#### Solution to the Business Problem

Link: (https://drive.google.com/drive/folders/1mcRFsxBf7bZc12X7Zoq9z5C9n5o-42Db?usp=share_link)
