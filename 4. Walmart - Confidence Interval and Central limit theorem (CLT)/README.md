# Walmart - Confidence Interval and Central limit theorem (CLT)

Walmart is an American multinational retail corporation that operates a chain of supercenters, discount departmental stores, and grocery stores from the United States. Walmart has more than 100 million customers worldwide.

#### Business Problem

The Management team at Walmart Inc. wants to analyze the customer purchase behavior (specifically, purchase amount) against the customer’s gender and the various other factors to help the business make better decisions. They want to understand if the spending habits differ between male and female customers: Do women spend more on Black Friday than men? (Assume 50 million customers are male and 50 million are female).

#### Dataset

The company collected the transactional data of customers who purchased products from the Walmart Stores during Black Friday. The dataset has the following features:
Dataset link: (https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/293/original/walmart_data.csv?1641285094)

User_ID:	User ID
Product_ID:	Product ID
Gender:	Sex of User
Age:	Age in bins
Occupation:	Occupation(Masked)
City_Category:	Category of the City (A,B,C)
StayInCurrentCityYears:	Number of years stay in current city
Marital_Status:	Marital Status
ProductCategory:	Product Category (Masked)
Purchase:	Purchase Amount

#### Problem Scenarios

1) Import the dataset and do usual data analysis steps like checking the structure & characteristics of the dataset.
2) Detect Null values & Outliers (using boxplot, “describe” method by checking the difference between mean and median, isnull etc.)
3) Do some data exploration steps like:
   - Tracking the amount spent per transaction of all the 50 million female customers, and all the 50 million male customers, calculate the average, and conclude the results.
   - Inference after computing the average female and male expenses.
   - Use the sample average to find out an interval within which the population average will lie. Using the sample of female customers you will calculate the interval within which the average spending of 50 million male and female customers may lie.
4) Use the Central limit theorem to compute the interval. Change the sample size to observe the distribution of the mean of the expenses by female and male customers.
   - The interval that you calculated is called Confidence Interval. The width of the interval is mostly decided by the business: Typically 90%, 95%, or 99%. Play around with the width parameter and report the observations.
5) Conclude the results and check if the confidence intervals of average male and female spends are overlapping or not overlapping. How can Walmart leverage this conclusion to make changes or improvements?
6) Perform the same activity for Married vs Unmarried and Age
   - For Age, you can try bins based on life stages: 0-17, 18-25, 26-35, 36-50, 51+ years.
7) Give recommendations and action items to Walmart.

### Recommendation Based on Insights gathered:

**Business Insights**
- Male customers are significantly more than Females ie 75% of the users are Male and 25% are Female.
- Buyers with ages between 26 and 35 are significantly more than any other age category ie ~ 80% of the users are between the ages 18-50 (40%: 26-35, 18%: 18-25, 20%: 36-45).
- There are more buyers in City Category B than in the other two City Categories.
- Buyers who have spent 1 year in the city are significantly more than the buyers who have spent 2 years, 3 years, more than 4 years, and less than 1 year in the city ie 35% Staying in the city from 1 year, 18% from 2 years, 17% from 3 years.
- Unmarried buyers are more in numbers than married buyers ie 60% are single and 40% are married.
- Males in City Category C tend to spend more amount of money than all the other individual buyers.
- There are 20 product categories in total wherein 1, 5, 8, & 11 have the highest purchasing frequency.
- There are 20 different types of occupation in the city.
- With 90%, 95%, and even 99% of confidence levels, we can see that Male buyers spend significantly more money than Female Buyers since there is no overlap between confidence intervals.
- With 90%, 95%, and even 99% of confidence levels, we can see that Marital Status has no impact on spending.
- With 90%, 95%, and even 99% of confidence levels, we can see that buyers aged between 0-17, significantly spend less money than the other Buyers, since there is no overlap between confidence intervals.
- With 90%, 95%, and even 99% of confidence levels, we can see that buyers aged between 51-55, significantly spend more money than the other Buyers, since there is no overlap between confidence intervals.
- Products under categories 1, 5, and 8 generate a huge amount of revenue for Walmart.

**Confidence Interval**

- Confidence Interval by Gender 
  - Now using the Central Limit Theorem for the population:
1. Average amount spent by male customers is 9,85,830.10
2. Average amount spent by female customers is 8,07,370.73
  - Now we can infer about the population that, 95% of the time:
1. Average amount spent by the male customer will lie in between: (895617.83, 955070.97)
2. Average amount spent by the female customer will lie between: (673254.77, 750794.02)

- Confidence Interval by Marital_Status
1. Married confidence interval of means: (806668.83, 880384.76)
2. Unmarried confidence interval of means: (848741.18, 912410.38)

- Confidence Interval by Age
1. For age 26-35 --> confidence interval of means: (945034.42, 1034284.21)
2. For age 36-45 --> confidence interval of means: (   823347.80, 935983.62)
3. For age 18-25 --> confidence interval of means: (   801632.78, 908093.46)
4. For age 46-50 --> confidence interval of means: (   713505.63, 871591.93)
5. For age 51-55 --> confidence interval of means: (   692392.43, 834009.42)
6. For age 55        --> confidence interval of means: (   476948.26, 602446.23)
7. For age 0-17    --> confidence interval of means: (   527662.46, 710073.17)

**Business Recommendation**

- Men spent more money than women, So the company should focus on retaining male customers and getting more male customers.
- Could probably create an additional offer for female buyers, so that the no.of potential female buyers would increase, and hence the average spend would also increase for female buyers.
- Product_Category - 1, 5, 8, & 11 have the highest purchasing frequency. it means these are the products in these categories are liked more by customers. The company can focus on selling more of these products or selling more of the products which are purchased less.
- The Average spending of married and unmarried are too close to each other. So, the differentiation between them is very low. Hence, an equal approach to target married and unmarried customers would be advised. Both couple-type products and other products will get sold based on the data given.
- Unmarried customers spend more money than married customers, So the company should focus on the acquisition of Unmarried customers.
- Customers in age 18-45 spend more money than others, So the company should focus on the acquisition of customers who are in aged 18-45
- Male customers living in City_Category C spend more money than other male customers living in B or C, Selling more products in City_Category C will help the company increase its revenue.
- Walmart should invest in advertisements for expensive products to target male buyers in city category C.
- Walmart should collaborate with celebrities to promote male products.
- Walmart should invest in targeted advertisements for individual buyers aged between 51-55.
- Walmart should engage in different marketing campaigns to target individual buyers in city category B.
- Walmart should invest in ad campaigns to boost sales of products categorized under 1, 5, and 8 product categories.

#### Solution to the Business Problem

Link: (https://drive.google.com/drive/folders/1ZjqcNSWsj_618WDkJhG_lBIKazCksEcJ?usp=share_link)
