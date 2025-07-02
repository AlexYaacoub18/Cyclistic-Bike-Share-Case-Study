AA# Cyclistic_bike_share_case_study
# Introduction
The **Cyclistic Bike Share Case Study** is a capstone project for the Google Data Analytics Professional Certificate on Coursera. In this project, I will follow the data analysis process, which will <ins>ask, prepare, process, analyze, share, and act</ins>, to analyze the data. 
# Background
Cyclistic is a bike-share program based in Chicago, launched in 2016. Since its inception, it has expanded to include a fleet of 5,824 geotracked bicycles and 692 docking stations throughout the city. Users can unlock a bike from any station and return it to any other station in the network at their convenience.

The company offers flexible pricing options, including single-ride passes, full-day passes, and annual memberships. Riders who choose single-ride or full-day passes are considered casual riders, while those who purchase annual memberships are classified as Cyclistic members.

Financial analysis has shown that annual members generate more long-term revenue compared to casual riders. As a result, the company is shifting its focus toward converting casual riders into members. To support this strategy, the marketing team is exploring how casual riders and annual members differ in their usage patterns and what factors might encourage casual riders to become members. Historical trip data is being analyzed to uncover trends and inform targeted marketing efforts.
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
- Manually went through each Excel file and cleared any null rows utilizing the conditional formatting feature
- Created a new column ride_length subtracting the values from started_at & ended_at to get the ride duration
- Added a day_of_week column using the weekday command

### Data Combining
- Uploaded the 12 datasets to SQL BigQuery and used the WITH...AS and UNION ALL commands to create a temporary table titled "combined_data" and merge all the 12 months datasets, showcasing only the following columns: (ride_length, member_casual, day_of_week, rideable_type, ride_month)

## Analyze
### Data Analysis
The analysis question was:
#### How do annual members and casual riders use Cyclistic Bikes differently?

##### - <ins>Total Rides 2024/2025<ins/>
The figure below shows the total number of rides carried out by Cyclistic members and casual riders in 2024/2025:

<img width="346" alt="Screen Shot 2025-06-28 at 8 34 27 AM" src="https://github.com/user-attachments/assets/762a7888-0803-4e73-9fec-c7f18a6af3d8" />

- Cyclistic members recorded a greater bicycle activity than casual riders. The total rides for Cyclistic members is 523,323, while 254,096 trips are for casual riders
- Cyclistic members accounted for about 67.61% of total rides, whereas casual riders made up 32.39% of total rides in that 12-month period

##### - <ins>Types of Bikes<ins/>
The figure below shows the different types of bikes used for the duration of the 12 months for both member and casual members:

<img width="1005" alt="Screen Shot 2025-06-28 at 8 33 52 AM" src="https://github.com/user-attachments/assets/b67d43ea-c839-46eb-bf31-5b331980c31f" />

- There are three types of bicycles: classic bikes, electric bikes, and electric scooters
- Cyclistic members and casual riders prefer to show a higher preference for electric bicycles over classic bicycles
- More annual members are using the classic and electric bikes, whereas more casual riders are using the electric scooters

##### - <ins>Average ride duration<ins/>
The average ride length is plotted against the type of users (member vs. casual):

<img width="1039" alt="Screen Shot 2025-06-28 at 8 33 21 AM" src="https://github.com/user-attachments/assets/e4aaa09b-7665-4dab-8858-e6141fa202b6" />


- Casual riders have an average ride duration of 18.327 minutes, whereas annual members have a smaller average ride duration of 11.442 minutes. Hence, the disparity between casual and member riders is almost double

##### - <ins>Total rides taken in a month<ins/>
The preference for cycling activity can be determined by drawing a graph of trips taken against the month from January to December 2022:

<img width="872" alt="Screen Shot 2025-06-28 at 8 30 36 AM" src="https://github.com/user-attachments/assets/4e55e406-b7f4-454f-918c-345138909b42" />

- Total riders every month seem pretty consistent, which might indicate an issue with growth in the market
- We do see a slight fluctuation with an increase in casual and a decrease in member riders between July and November 2024
- The month with the largest member count of 54,844 was in February 2025
- The month with the largest casual rider count of 32,103 was in August 2025

##### - <ins>Average monthly ride duration <ins/>
The mean trip duration is depicted in the line graph below:

<img width="877" alt="Screen Shot 2025-06-28 at 8 31 15 AM" src="https://github.com/user-attachments/assets/22c2709c-1bc3-4f54-9fea-5a4e17f25dc8" />

- The monthly average ride duration for annual members is the highest in July (13.53 minutes)
- For casual riders, the highest mean trip duration is in May (25.68 minutes)

##### - <ins>Total rides taken in a week<ins/>
The bar chart below is used to study the daily user activity over a week:

<img width="669" alt="Screen Shot 2025-06-28 at 8 44 23 AM" src="https://github.com/user-attachments/assets/675fb3d5-cb45-4c41-b0ea-49e2ea7834d8" />

- The highest volume of riders would occur on Fridays
- Annual members have the highest activity (85,434 rides) on Wednesdays and the lowest activity (56,952 rides) on Sundays
- Casual riders have the greatest activity (49,885 rides) on Saturdays and the lowest activity (28,104 rides) on Tuesdays

##### - <ins>Average weekly ride duration<ins/>
The mean ride duration across the week is displayed as follows:

<img width="727" alt="Screen Shot 2025-06-28 at 8 46 08 AM" src="https://github.com/user-attachments/assets/c6e4155e-2a70-423b-8fb9-bb5bc4d290f4" />

- Annual members cycled the longest on Sunday with an average ride length of 12.64 minutes
- Casual riders cycled the longest on Sunday, with an average ride length of 21.41 minutes

## Share

<img width="669" alt="Screen Shot 2025-06-28 at 8 31 57 AM" src="https://github.com/user-attachments/assets/16f47b6c-232f-4a97-8cb2-021f21e2f420" />

View [Cyclistic Bike Share Dashboard](https://public.tableau.com/views/Ride_Project/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).

The analysis on the similarities and differences between annual member riders and casual riders is presented as such on the dashboard above 

**Similarities:**
- Both Cyclistic members and casual riders prefer riding during the spring and summer months (June to September).
- Ride activity declines in colder months, likely due to less favorable weather conditions.
- Both groups primarily use classic and electric bikes, with very little usage of electric scooters.
- Average ride duration is higher on weekends for both casual and member riders.

**Differences:**
- Casual riders have longer average ride durations (18.33 minutes) than member riders (11.44 minutes).
- Casual riders prefer electric bikes, while member riders use classic bikes more frequently.
- Member ride activity is consistent throughout the week, suggesting commuting or utility use.
- Casual riders show higher usage on weekends and lower on weekdays, indicating more recreational or leisure usage.

## Act

### Recommended Strategies to Convert Casual Riders into Cyclistic Members

#### <ins>Flexible Membership Plans<ins/>
- Introduce multiple membership tiers such as daily ($3), monthly ($30 to $45), and annual ($365) to meet the needs of different rider types.  
- Casual riders who bike occasionally or seasonally may be more likely to join if there are low-commitment options available.

#### <ins>Weekend-Focused Promotions<ins/>
- Since casual riders are most active on weekends, offer special weekend-only promotions that encourage trying out membership.  
- For example, consider launching offers like a "Weekend Pass" or "Free Trial Ride for First-Time Members."

#### <ins>Electric Bike Incentives<ins/>
- Casual riders prefer electric bikes more than member riders.  
- Promote membership benefits such as lower e-bike rates or early access to electric bikes to appeal to this group.

#### <ins>Ride More, Save More Loyalty Program<ins/>
- Create a loyalty program where all users earn points for each ride, but only members can redeem those points for rewards such as ride credits or discounts.  
- This adds value to becoming a member while still engaging casual users.

#### <ins>Seasonal Membership Campaigns<ins/>
- Use seasonal trends to launch timely membership drives.  
- For instance, introduce a "Spring into Cycling" campaign with discounted sign-ups and extra perks like bonus ride minutes for new members.

#### <ins>Weekday Commuter Trials<ins/>
- Casual riders ride less during weekdays, so encourage weekday use through targeted promotions.  
- Offer morning or weekday-only discounts to show casual riders the benefit of using bikes for daily routines like commuting or errands.

#### <ins>Community Engagement and Events<ins/>
- Host fun, member-centered events such as group rides, city scavenger hunts, or themed cycling days.  
- Allow casual riders to participate as guests to experience the community aspect of membership.  
- Promote these events on social media with member testimonials and photos to build excitement and encourage conversions.

# Conclusion
This analysis highlights the key differences in how casual and member riders use Cyclistic bikes. By designing targeted strategies that address casual riders' preferences and behavior, such as their love for electric bikes, weekend activity, and longer ride durations, Cyclistic can successfully motivate more casual users to become members.
