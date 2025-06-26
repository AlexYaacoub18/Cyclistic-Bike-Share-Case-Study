# Cyclistic-Bike-Share-Case-Study
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
1. [Data Cleaning](https://github.com/AlexYaacoub18/Cyclistic-Bike-Share-Case-Study/blob/main/Data%20Cleaning)
2. [Data Combining](https://github.com/AlexYaacoub18/Cyclistic-Bike-Share-Case-Study/blob/main/Data%20Combining)
3. [Data Analysis](https://github.com/AlexYaacoub18/Cyclistic-Bike-Share-Case-Study/blob/main/Data%20Analysis)
### Data Cleaning
- Manually went through each Excel file and cleared any null rows utilizing the conditional formatting feature.
- Created a new column ride_length subtracting the values from started_at & ended_at to get the ride duration
- Added a day_of_week column using the weekday command
### Data Combining
- Uploaded the 12 datasets to SQL BigQuery and used the WITH...AS and UNION ALL statements to create a temporary table titled as "combined_data" and merges all the 12 months datasets showcasing only the following columns: (ride_length, member_casual, day_of_week, rideable_type, 'June' AS ride_month)
### Data Analysis
