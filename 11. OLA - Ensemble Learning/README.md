## 10. OLA - Ensemble Learning
Recruiting and retaining drivers is seen by industry watchers as a tough battle for Ola. Churn among drivers is high and it’s very easy for drivers to stop working for the service on the fly or jump to Uber depending on the rates.

As the companies get bigger, the high churn could become a bigger problem. To find new drivers, Ola is casting a wide net, including people who don’t have cars for jobs. But this acquisition is costly. Losing drivers frequently impacts the morale of the organization and acquiring new drivers is more expensive than retaining existing ones.

#### Business Problem

You are working as a data scientist with the Analytics Department of Ola, focused on driver team attrition. You are provided with the monthly information for a segment of drivers for 2019 and 2020 and tasked to predict whether a driver will be leaving the company or not based on their attributes like

Demographics (city, age, gender etc.)
Tenure information (joining date, Last Date)
Historical data regarding the performance of the driver (Quarterly rating, Monthly business acquired, grade, Income)

#### Business Insights
A. There are more Male drivers than Female drivers.
B. 99.7% drivers didn't get income raise or grade raise.
C. 88.54% of drivers saw their rating getting improved.
D. 30.67% of drivers left OLA.
E. Number of drivers joining OLA increased significantly since 2018.
F. Male drivers have lost more rating compared to Female drives.
G. Drivers who:
   - worked for more years with OLA
   - older in age
   - have lower education
   - have very high ratings
   - generated high total revenue for OLA, Saw their income and grade increased significantly compared to other drivers.
H. Drivers with higher grade and higher ratings left OLA more in numbers compared to other drivers.
I. Most of the drivers who left OLA had joined OLA in recent years compared other drivers who decided to stay and not leave OLA.
J. Surprisingly, most of the drivers who left OLA have their last reporting month and year as December 2020.
K. Test model accuracy achieved for 'Bagging' and 'Boosting' is 95% and 94% respectively.
L. Area under ROC-AUC curve for 'Bagging' and 'Boosting' is 95% and 96% respectively.
M. F1-Score is betwwen 95% for both 'Bagging' and 'Boosting' models and for both target labels.
N. Precision and Recall Scores are between 94% to 96% for both 'Bagging' and 'Boosting' models and for both target labels.
O. Churning of the drivers is most affected by reporting_end_month, reporting_end_year, joining_month and age in this exact order from highest importance to lowest.
   - There are 57% male employees and 43% female employees.
   - The percentages of employees with different education levels are almost same for level 1 & 2.
   - 97.3% of the employees who did not get a raise.
   - Almost 43% of the employees joined at lowest designation (1). 34% joined at level 2, 20% at level 3 and below 2% joined at higher levels.
   - Majority (35%) of the employees currently are at designation level 2, followed by designation level 1 (31%) and 3 (26%). Less than 5% of the employees are currently in higher designations.
   - Only 54.6% of the employees received a promotion, while 45.4% did not. However, only 2.6% received a raise in income.
   - Number of employees has been increase with increase in year as well as number of reportings.
   - The majority of the employees seem to be associated with city C20.
   - Scatter plot of Income shows that Income increases with increase in age but after 45-50, we see a subtle decline.
   - Scatter plot of Total Business Value shows an increase with increase in Age yet we notice a decline after 45.
   - Income decreses with increase in Destination as about 4% of the employees hold higher designations.
   - The median of the Income for employees having higher Grades is greater.
   - Distribution of Income for enployes at different Education level is about a change of 3-5% with level 0.
   - Joining Designation Increases with increase in Grade.
   - Top reporting days is 24 days.
   - About 55% of the reportings of the employees has got Quarlerly Rating 1.
   - Number of reportings increases with increase in Income as well as Total Business Value.
   - Recall increased after treatment of data imbalance and is performing bettee in Gradient Boosting.
   - Precision dropped after treatment of data imbalance and is performing better in Random Forest.
   - F1_score incresed after the treatment of imabalanced data and in Gradient Boosting.

#### Recommendation 
A. To predict the chrning of the driver, the columns reporting_end_month, reporting_end_year, joining_month, and age should be considered.
B. More data points should be gathered to analyze why many drivers who reported last in December 2020 left OLA.
C. We saw that the high performing drivers leave more often than the rest. OLA can start a program to reward high performers and recognize their work more often.
D. OLA can conduct periodic surveys to obtain more data points so as to make the prediction model better and more accurate.
F. We could also see that the drivers who joined OLA recently, left in more numbers. So OLA can focus more on these new drivers to make them stop leaving.  


#### Solution to the Business Problem 
https://drive.google.com/file/d/1wmZ_Mj5d3Ds4ThlNZzlbeWYw3fOwPoPa/view?usp=sharing


