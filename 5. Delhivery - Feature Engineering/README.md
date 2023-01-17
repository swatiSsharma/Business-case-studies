# Delhivery - Feature Engineering 

Delhivery is the largest and fastest-growing fully integrated player in India by revenue in Fiscal 2021. They aim to build the operating system for commerce, through a combination of world-class infrastructure, logistics operations of the highest quality, and cutting-edge engineering and technology capabilities.  

The Data team builds intelligence and capabilities using this data that helps them to widen the gap between the quality, efficiency, and profitability of their business versus their competitors.

#### Business Problem

- The company wants to understand and process the data coming out of data engineering pipelines:

  >• Clean, sanitize and manipulate data to get useful features out of raw fields
  >• Make sense out of the raw data and help the data science team to build forecasting models on it.

#### Dataset

The company collected the transactional data of customers. The dataset has the following features:
Dataset link: (https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/551/original/delhivery_data.csv?1642751181)

#### Column Profiling

- data :  tells whether the data is testing or training data
- trip_creation_time : Timestamp of trip creation
- route_schedule_uuid : Unique Id for a particular route schedule
- route_type : Transportation type 
    - FTL – Full Truck Load: FTL shipments get to the destination sooner, as the truck is making no other pickups or drop-offs along the way
    - Carting: Handling system consisting of small vehicles (carts)
- trip_uuid : Unique ID given to a particular trip (A trip may include different source and destination centers)
- source_center : Source ID of trip origin
- source_name : Source Name of trip origin
- destination_cente : Destination ID
- destination_name : Destination Name
- od_start_time : Trip start time
- od_end_time : Trip end time
- start_scan_to_end_scan : Time taken to deliver from source to destination
- is_cutoff : Unknown field
- cutoff_factor : Unknown field
- cutoff_timestamp : Unknown field
- actual_distance_to_destination : Distance in Kms between source and destination warehouse
- actual_time : Actual time taken to complete the delivery (Cumulative)
- osrm_time : An open-source routing engine time calculator which computes the shortest path between points in a given map (Includes usual traffic, distance through major and minor roads) and gives the time (Cumulative)
- osrm_distance : An open-source routing engine which computes the shortest path between points in a given map (Includes usual traffic, distance through major and minor roads) (Cumulative)
- factor : Unknown field
- segment_actual_time : This is a segment time. Time taken by the subset of the package delivery
- segment_osrm_time : This is the OSRM segment time. Time taken by the subset of the package delivery
- segment_osrm_distance : This is the OSRM distance. Distance covered by subset of the package delivery
- segment_factor : Unknown field

#### Problem Scenarios

In-depth analysis and feature engineering to be done : 
    
    > - time taken between od_start_time and od_end_time 
    > - hypothesis testing/ Visual analysis : population mean of start_scan_to_end_scan & time taken between od_start_time and od_end_time
    > - hypothesis testing/ visual analysis :
            - actual_time aggregated value and OSRM time aggregated value 
    > - hypothesis testing/ visual analysis :
            - actual_time aggregated value and segment actual time 
    > - hypothesis testing/ visual analysis : 
            - osrm distance aggregated value and segment osrm distance 
    > - hypothesis testing/ visual analysis :
            - osrm time aggregated value and segment osrm time aggregated value
    > - outliers in the numerical variables 
    > - outliers using the IQR method.
    > - one-hot encoding of categorical variables (like route_type)
    > - Normalize/ Standardize the numerical features using MinMaxScaler or StandardScaler.

#### Inferences and Recommendations

**Insights and Observations**

- 14817 different trips happened between source to destinations during 2018 , September and October.
- 1504 delivery routes on which trips are happening.
- we have 1508 unique source centers and 1481 unique destination centers
- From 14817 total different trips , we have  8908 (60%) of the trip-routes are Carting , which consists of small vehicles and 5909 (40%) of total trip-routes are FTL : which are Full Truck Load get to the destination sooner. as no other pickups or drop offs along the way .

**Hypothesis tests Results**

From 2 sample t-test ,we can also conclude that 

    - Average time_taken_btwn_odstart_and_od_end for population is equal to Average start_scan_to_end_scan for population.
    - population average actual_time is less than population average start_scan_to_end_scan.
    - population mean Actual time taken to complete delivery and population mean time_taken_btwn_od_start_and_od_end are also not same.
    - Mean of actual time is higher than Mean of the OSRM estimated time for delivery
    - Population average for Actual Time taken to complete delivery trip and segment actual time are same.
    - Average of OSRM Time & segment-osrm-time for population is not same   
    - Population Mean osrm time is less than Population Mean segment osrm time.
    - Average of OSRM distance for population is less than average of segment OSRM distance
    - population OSRM estimated distance is higher than the actual distance from source to destination warehouse.

**From Exploratory Data Analysis**

    - we can observe that Mumbai Maharashtra ,Delhi , Gurgaon(Haryana),Bengaluru Karnataka ,Hyderabad Telangana, Chennai Tamil Nadu, Ahmedabad-Gujarat, Pune Maharashtra, Chandigarh Chandigarh and Kolkata West Bengal are some cities have highest amount of trips happening states with in the city. 
    - If we talk about , not having equal source and destination states , source and destination cities having highest number of trips in between are : Delhi TO Gurgao ,  Gurgaon  TO Bengaluru ,  Bhiwandi/Mumbai TO Pune Maharashtra ,    Sonipat TO    Gurgaon, Haryana
    - It is also been observed that lots of deliveries are happening to airports  like : Chennai to MAA Chennai international Airport , Pune to Pune Airport (PNQ),Kolkata to    CCU West Bengal Kolkata International Airport , Bengaluru to BLR-Bengaluru International Airport etc. 
    - From Bar charts , and calculated tables in analysis , we can observe that highest trips are happening is with in the particular cities, in terms of average distance between destinations , we can observe Guwahati to Mumbai , Bangalore to Chandigarh ,Bangalore to Delhi , Benglore to Gurgaon are the longest routes.
    - The source to destination city routes having largest numbers of trip happening having large distances :
        - Guwahati TO Bhiwandi, Bengaluru TO Chandigarh, Bengaluru TO Delhi, Gurgaon TO MAA Chennai Airport, Bhiwandi TO Kolkata, Bengaluru TO Kolkata, Gurgaon TO Hyderabad, Gurgaon TO Kolkata
    - The routes which covered multiple cities in between source and destination :
        - Most covered cities routes are : Guwahati TO Lakhimpur , Jaipur TO Tanru , Guwahati TO Tura , Mangalore TO Udupi , Ajmer TO Raipur , Mainpuri TO Tilhar . which passes through  more than 8 cities.
    - Routes which are busiest from source to destinations and states in which highest activities are noticed :
        - Delhi to Haryana is the busiest route, having more than 400 trips in between. Some of such busy routes are Haryana to Uttar Pradesh , Chandigarh to Punjab , Delhi to Uttar Pradesh . 
        - Within the state , Maharashtra , Karnataka, Tamil Nadu, Haryana, Telangana, Gujarat , West Bengal and Uttar Pradesh are some states having above 1000 trips. 
    - Some warehouse having Maximum traffic and hence busiest junctions. 
        - Bengaluru Karnataka, Gurgaon Haryana, Mumbai Maharashtra, Hyderabad Telangana, Delhi, Pune Maharashtra, Chandigarh Punjab, Chennai Tamil Nadu, Sonipat Haryana, Kolkata West Bengal, Ahmedabad Gujarat, MAA Tamil Nadu, Jaipur Rajasthan, Kanpur Uttar Pradesh, Surat Gujarat, Muzaffrpur Bihar, FBD Haryana, Bhopal Madhya Pradesh, Noida Uttar Pradesh.

Recommendations 

    - As per analysis, It is recommended to use Carting (small vehicles) for delivery with in the city in order to reduce the delivery time, and Heavy trucks for long distance trips or heavy load. based on this , we can optimize the delivery time as well as increase the revenue as per requirements. 
    - Increasing the connectivity in tier 2 and tier 3 cities along with profession tie-ups with several e-commerce giants can increase the revenue as well as the reputation on connectivity across borders. 
    - We can work on  optimizing the scanning time on both ends which is start scanning time and end scanning time so that the delivery time can be equated to the OSRM estimated delivery time.
    - For longer trips (both in terms of time and distance) FTL trips should be preferred.
    - More trips should start between evening and early mornings.
    - 'osrm distance' should be used as estimations of the actual trip distances.
    - 'osrm time' should be used as estimations of the actual trip times.
    - 'od_time_elapsed' should be used as estimations of start_scan_to_end_scan.

#### Solution to the Business Problem

Link: (https://drive.google.com/drive/folders/1SvivcISkkiDvWcFmYUstF3Vf2iiITbQC?usp=share_link)
