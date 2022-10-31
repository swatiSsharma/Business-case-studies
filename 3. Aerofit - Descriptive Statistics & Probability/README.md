# Aerofit - Descriptive Statistics & Probability

Aerofit is a leading brand in the field of fitness equipment. Aerofit provides a product range including machines such as treadmills, exercise bikes, gym equipment, and fitness accessories to cater to the needs of all categories of people.

#### Business Problem

The market research team at AeroFit wants to identify the characteristics of the target audience for each type of treadmill offered by the company, to provide a better recommendation of the treadmills to the new customers. The team decides to investigate whether there are differences across the product with respect to customer characteristics.

  - Perform descriptive analytics **to create a customer profile** for each AeroFit treadmill product by developing appropriate tables and charts.
  - For each AeroFit treadmill product, construct **two-way contingency tables** and compute all **conditional and marginal probabilities** along with their insights/impact on the business.

#### Dataset

The company collected the data on individuals who purchased a treadmill from the AeroFit stores during the prior three months. The dataset has the following features:

Dataset link: (https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/125/original/aerofit_treadmill.csv?1639992749)

Product Purchased:	KP281, KP481, or KP781
Age:	In years
Gender:	Male/Female
Education:	In years
MaritalStatus:	Single or partnered
Usage:	The average number of times the customer plans to use the treadmill each week.
Income:	Annual income (in $)
Fitness:	Self-rated fitness on a 1-to-5 scale, where 1 is the poor shape and 5 is the excellent shape.
Miles:	The average number of miles the customer expects to walk/run each week

**Product Portfolio:**

- The KP281 is an entry-level treadmill that sells for $1,500.
- The KP481 is for mid-level runners that sell for $1,750.
- The KP781 treadmill is having advanced features that sell for $2,500.

#### Problem Scenarios:

- 1. Import the dataset and do usual data analysis steps like checking the structure & characteristics of the dataset
- 2. Detect Outliers (using boxplot, “describe” method by checking the difference between mean and median)
- 3. Check if features like marital status, age have any effect on the product purchased (using countplot, histplots, boxplots etc)
- 4. Representing the marginal probability like - what percent of customers have purchased KP281, KP481, or KP781 in a table (can use pandas.crosstab here)
- 5. Check correlation among different factors using heat maps or pair plots.
- 6. With all the above steps you can answer questions like: What is the probability of a male customer buying a KP781 treadmill?
- 7. **Customer Profiling** - Categorization of users.
- 8. **Probability** - marginal, conditional probability.
- 9. Some recommendations and actionable insights, based on the inferences.

#### Insights & Recommendation:

**Business Insights:**

- A. People with higher incomes prefer to buy KP781 over other products.
- B. People with lower and middle income prefer to buy KP281 and KP481 over the other products.
- C. People with higher fitness levels prefer to buy KP781 over other products.
- D. People with lower and middle fitness levels prefer to buy KP281 and KP481 over the other products.
- E. People who expect extensive use of the product prefer to buy KP781 over the other products.
- F. People who expect less extensive use of the product prefer to buy KP281 and KP481 over the other products.
- G. Marital Status seems to have no apparent effect on individual preferences to buy different products.
- H. Males prefer to buy KP781 significantly more than Women.
- I. Females prefer to buy KP281 and KP481 significantly more than Men.
- J. People with higher education prefer to buy KP781 over other products.
- K. People with lower and middle education prefer to buy KP281 and KP481 over the other products.
- L. Individuals with Ages between 20-30 are more likely to buy any of the products than other Age groups.

**Business Recommendations:**

- A. Aerofit should target selling KP781 products to men with higher fitness levels, higher income, and higher education.
- B. Aerofit should target selling KP281 and KP481 products to individuals with average or below-average fitness levels, income, and education.
- C. Aerofit should target selling the KP781 product to the people who are expecting more extensive usage of the product.
- D. Aerofit should target selling KP281 and KP481 products to the people who are expecting less extensive usage of the product.
- E. Aerofit should target selling products to people who are aged between 20-30 years, more than other age groups. Targeted advertisements should be used for the same.

#### Solution to the Business Problem

Link: (https://drive.google.com/drive/folders/1t-catAslfYOw2JGEblQFme3OdHo5rIoo?usp=share_link)
