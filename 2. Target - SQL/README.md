## 2.  Target - SQL

Target is one of the world’s most recognized brands and one of America’s leading retailers. Target makes itself a preferred shopping destination by offering outstanding value, inspiration, innovation and an exceptional guest experience that no other retailer can deliver.

#### Business Problem

This business case has information of 100k orders from 2016 to 2018 made at Target in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers.



### Dataset

Dataset link: https://drive.google.com/drive/folders/1TGEc66YKbD443nslRi1bWgVd238gJCnb

Data is available in 8 csv files:

1. customers.csv

2. geolocation.csv

3. order_items.csv

4. payments.csv

5. reviews.csv

6. orders.csv

7. products.csv

8. sellers.csv

#### Problem Scenarios

- **1. Import the dataset and do usual exploratory analysis steps like checking the structure & characteristics of the dataset**

  - Data type of columns in a table
  - Time period for which the data is given
  - Cities and States covered in the dataset

- **2. In-depth Exploration:**

  - Is there a growing trend on e-commerce in Brazil? How can we describe a complete scenario? Can we see some seasonality with peaks at specific months?
  - What time do Brazilian customers tend to buy (Dawn, Morning, Afternoon or Night)?

- **3. Evolution of E-commerce orders in the Brazil region:**

  - Get month on month orders by region, states
  - How are customers distributed in Brazil

- **4. Impact on Economy: Analyze the money movemented by e-commerce by looking at order prices, freight and others.**

  - Get % increase in cost of orders from 2017 to 2018 (include months between Jan to Aug only)
  - Mean & Sum of price and freight value by customer state

- **5. Analysis on sales, freight and delivery time**

  - Calculate days between purchasing, delivering and estimated delivery
  - Create columns:
     - time_to_delivery = order_purchase_timestamp-order_delivered_customer_date
     - diff_estimated_delivery = order_estimated_delivery_date-order_delivered_customer_date
  - Group data by state, take mean of freight_value, time_to_delivery, diff_estimated_delivery
  - Sort the data to get the following:
     - Top 5 states with highest/lowest average freight value - sort in desc/asc limit 5
     - Top 5 states with highest/lowest average time to delivery
     - Top 5 states where delivery is really fast/ not so fast compared to estimated date

- **6. Payment type analysis:**

  - Month over Month count of orders for different payment types
  - Distribution of payment installments and count of orders

#### Insights & Recommendation:

 **All Insights :**

1) Customers' informationâ€™s:

A·        We have 99,441 customers of data available, out of which 96096 Unique Customers IDs with 14994 different locations of customers
B·        Customers are from different 4119 cities and 27 states in Brazil
C·        From a total of 99441 orders, 1107 are shipped, 625 were canceled, and 96478 are delivered
D·        68% of customers are from southeast Brazil, 14% are from south Brazil and the rest are from other regions of Brazil

2) Analysis of sales and revenue as per time:

A·        Time period for which the data is given is 25 months
B·        As compared to 2017 the revenue has increased in 2018 by 21%
C·       The Average number of orders is higher during the month of November. September and October have comparatively low orders on average whereas May, July, and August have a higher number of average orders compared to other months.
D·        Tuesday, Monday and Wednesdays have a relatively higher number of orders

3) Increasing trend:

A·        There is an increasing trend in orders, trend sustains during 2018. There is a slight fall we can observe during October 2017 followed by a great hike in November month and again a fall at end of December 2017 and January 2018.
B·        We can observe the trend of increasing orders with time and also for revenue.
C·        We can observe there's an 81.5% growth increase in terms of orders and a 70.7% growth increment in terms of revenue in January from 2017 to 2018.
D·        Growth rate for July and August from 2017 to 2018 is relatively very low whereas 2017-February, march, and November were the highest growing sale month in comparison to the previous month.

4) Customer_purchasing Behavior:

A·        Customers are purchasing orders from morning 8 am till late evening 11 pm.
B·        Afternoon and evening orders are very high as compared to the morning, and night time. 

5) Delivery time:

A·        After the purchase is made, the average time for approving the order by the seller is 0.26 days and the median time is 0, which means within a day.
B·        Average time taken for a carrier to start the delivery is 2 and a half days.
C·        Average time taken to complete delivery is 12 days and the median delivery time is 10 days.
D·        Estimated time delivery average is 23 days.
E·        There is a positive correlation between freight value and delivery time.
F·        Long-distance deliveries are having higher freight values and also take more time for delivery
G·        States SÃ£o Paulo, ParanÃ¡, Minas Gerais, Distrito Federal, Santa Catarina, and Rio de Janeiro are some of the states having relatively faster delivery times.
H·        Alagoas, Amazonas, AmapÃ¡, ParÃ¡, and Roraima are some states that have relatively very slow delivery times.

6) Region and State-wise Analysis :

A·        SÃ£o Paulo, Rio de Janeiro, Minas Gerais, Rio Grande do Sul, and ParanÃ¡ are the top 5 highest orders states and also generate the highest revenue.
B·        More than 80% of orders are coming from south, southeast, and northeast Brazil. 90% of the revenue is coming from south, southeast, and northeast Brazil

7) Payment type-related info :

A·        78% of payments are done using a credit card and 17.92% are done with UPI.
B·        Majority of the orders are purchased at 1 payment installment.
C·        More than 5 installments purchases are relatively very low.


**Recommendations:**

1.      From the distribution and statistical analysis we can observe the average time to complete the delivery is 12 days. which should be reduced to at least half, as due to high competition in the e-commerce market, it is vital to do so
2.      In order to reduce the delivery time, if we look at the average time for the carrier to start the delivery itself takes at least 2 and a half days and the order approval time is 0.26 days. These two should be optimized as low as possible, which can result in delivery faster.
3.      If we look at the Top states where delivery is really slow compared to the estimated date, they are all from the north Brazil region. Delivering faster in the northern states may create and increase new customers and revenue from the north.
4.      As per Analysis products belonging to the â€œbed table bathâ€ category are being sold max among all available categories, we could produce more items related to this category.
5.      Increasing the network in north Brazil, having small towns can help increase the customer base. As north Brazil has the worldâ€™s largest river and most extensive rain forest, must be a good travel destination, introducing necessary survival/ camping/adventure products can help increase revenue and order from the northern region
6.      As per the analysis Credit card payments are more. So target can give offers to customers paying with a credit card and can also give them an Interest-free EMI scheme.
7.      It was observed that an increasing trend in revenue and orders over time, yet during October and January sales are decreasing probably after Festival Sales. Introducing possible discounts on the not-so-running products can help sell more products during those low-going months.

#### Solution to the Business Problem

Link: (https://drive.google.com/drive/folders/1JMEBDIg8RdG4pXVG9KHDbcUGkh5VqzY_?usp=share_link)
