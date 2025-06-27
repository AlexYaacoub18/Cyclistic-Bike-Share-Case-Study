AA# Cyclistic-Bike-Share-Case-Study
# Introduction
The **Cyclistic Bike Share Case Study** is a capstone project for the Google Data Analytics Professional Certificate on Coursera. In this project, I will follow the data analysis process, which I learned from the course: <ins>ask, prepare, process, analyze, share, and act</ins>, to analyze the data. 
# Background
Cyclistic is a **bike-share company** based in Chicago that launched a successful bike-sharing program in 2016. Throughout the years, the program has expanded significantly to a fleet of 5,824 bicycles and a network of 692 geotracked stations sprawled across the city. With the large number of bicycles across numerous stations, customers can rent bikes from one station and return them to any other station within the network at their convenience. This encourages people to opt for cycling as a mode of transportation, therefore contributing to the success of Cyclistic's bike-sharing program. 

Cyclistic's marketing strategy has so far focused on building general awareness and appealing to broad consumer segments. The company offers flexible pricing plans that cater to the diverse needs of users, including single-ride passes, full-day passes, and annual memberships. Besides, it provides reclining bikes, hand tricycles, and cargo bikes, effectively welcoming individuals with disabilities and those who can't ride on the standard two-wheeled bicycles. Based on the company database, Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day. While traditional bikes remain the popular option, around 8% of users opt for the assistive alternatives. 

The company's marketing director believes that the company’s future success depends on maximizing the number of annual memberships. Therefore, as a junior data analyst, my team and I have to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, we will design a new marketing strategy to convert casual riders into annual members. 
# Approach / Steps
## ASK
### Business Task 
Design marketing strategies to **convert casual riders to members** by understanding how annual and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics.
### Guiding question to follow
*How do annual members and casual riders use Cyclistic bikes differently?* 
## PREPARE
### Data Source: 
[divvy-tripdata](https://divvy-tripdata.s3.amazonaws.com/index.html)
*TOOLS:* Excel (Process), SQL(Analyze), Tableau(Share)
## PROCESS
The basis for this analysis will be 12 months of bike data between the months of June 2024 and May 2025

The steps for processing are as follows:
1. Data Cleaning
2. [Data Combining](https://github.com/AlexYaacoub18/Cyclistic-Bike-Share-Case-Study/blob/main/Data%20Combining)
3. [Data Analysis](https://github.com/AlexYaacoub18/Cyclistic-Bike-Share-Case-Study/blob/main/Data%20Analysis)
### Data Cleaning
- Manually went through each Excel file and cleared any null rows utilizing the conditional formatting feature.
- Created a new column ride_length subtracting the values from started_at & ended_at to get the ride duration
- Added a day_of_week column using the weekday command

### Data Combining
- Uploaded the 12 datasets to SQL BigQuery and used the WITH...AS and UNION ALL statements to create a temporary table titled as "combined_data" and merges all the 12 months datasets showcasing only the following columns: (ride_length, member_casual, day_of_week, rideable_type, ride_month)
### Data Analysis
The analysis question was:
#### How do annual members and casual riders use Cyclistic Bikes differently?

##### - Total Rides 2024/2025
The figure below shows the total number of rides carried out by Cyclistic members and casual riders in 2024/2025:
<img width="256" alt="Screen Shot 2025-06-27 at 11 44 22 PM" src="https://github.com/user-attachments/assets/0d0994e4-c5bc-4d0c-8308-94d8f727f4d1" />
- Cyclistic members recorded a greater bicycle activity than casual riders. The total rides for Cyclistic members are 523,323, while 254,096 trips are for casual riders
- Cyclistic members accounted for about 67.61% of total rides, whereas casual riders made up 32.39% of total rides in that 12-month period

##### - Types of Bikes
The figure below shows the different types of bikes used for the duration of the 12 months for both member and casual members:
<img width="826" alt="Screen Shot 2025-06-28 at 12 24 51 AM" src="https://github.com/user-attachments/assets/6b2de160-91da-49b1-bbab-a78bbab6ba7b" />
- There are three types of bicycles: classic bikes, electric bikes, and electric scooters.
- Cyclistic members and casual riders prefer to show a higher preference for electric bicycles over classic bicycles.
- More annual members are using the classic and electric bikes, whereas more casual riders are using the electric scooters.

##### - Average ride duration
The average ride length is plotted against the type of users (member vs. casual):
<img width="837" alt="Screen Shot 2025-06-28 at 12 35 25 AM" src="https://github.com/user-attachments/assets/09ae35c3-3afc-4d98-b34e-2df9a6cab6ae" />
- Casual riders have an average ride duration of 18.327 minutes, whereas Annual members have a smaller average ride duration of 11.442 minutes. Hence, the disparity between casual and member riders is almost double.

##### - Total rides taken in a month
The preference of cycling activity can be determined by drawing the graph of trips taken against month from January to December 2022.
<img width="565" alt="Screen Shot 2025-06-28 at 1 11 48 AM" src="https://github.com/user-attachments/assets/2c7e9e23-bdfa-4bb8-be24-cdd224974a23" />
- Total riders every month seem pretty consistent, which might indicate an issue with growth in the market
- We do see a slight fluctuation with an increase in casual and a decrease in member riders between July and November 2024
- The month with the largest member count of 54,844 was in February 2025
- The month with the largest casual rider count of 32,103 was in August 2025

##### - Average monthly ride duration 
The mean trip duration is depicted in the line graph below.
<img width="654" alt="Screen Shot 2025-06-28 at 12 36 07 AM" src="https://github.com/user-attachments/assets/b1ef0089-e78f-4824-9e81-8d3620824905" />
- The monthly average ride duration for annual members is the highest in July (13.53 minutes).
- For casual riders, the highest mean trip duration is in May (25.68 minutes).

##### - Total rides taken on days of the week
The bar chart below is used to study the daily user activity over a week.
<img width="472" alt="Screen Shot 2025-06-28 at 12 36 27 AM" src="https://github.com/user-attachments/assets/012f1b0b-e59b-41e8-957c-7951bad65138" />
- The highest volume of riders would occur on Fridays
- Annual members have the highest activity (85,434 rides) on Wednesdays and the lowest activity (56,952 rides) on Sundays.
- Casual riders have the greatest activity (49,885 rides) on Saturdays and the lowest activity (28,104 rides) on Tuesdays.

##### - Average weekly ride duration
The mean ride duration across the week is displayed as follow.
<img width="475" alt="Screen Shot 2025-06-28 at 12 36 43 AM" src="https://github.com/user-attachments/assets/ab8d2f24-8125-4ada-b930-044787ba1bf3" />
- Annual members cycled the longest on Sunday with an average ride length of 12.64 minutes.
- Casual riders cycled the longest on Sunday with an average ride length of 21.41 minutes.

### Share
<img width="668" alt="Screen Shot 2025-06-28 at 1 09 07 AM" src="https://github.com/user-attachments/assets/ee27f6d5-29ee-43d6-ba1c-09f2618bb9c9" />

### Act
