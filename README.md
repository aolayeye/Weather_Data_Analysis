# surfs_up
## Overview
The Surf_Up analysis seeks to analyze weather for several years to determine if establishing a surfing business in oahu is viable. In this analysis, we woud utilize Jupyter notebook, a SQLite database, and VSCode where we will create our flask application to visualize the results of our analysis.

In the second part of our analysis, we will produce queries that show summary statistics for weather parameters for the months of June and December for multiple years.

## Control Flow
1. Import Dependencies: Matplotlib, NumPy and Pandas, Datetime, SQLAlchemy.
2. SQLAlchemy Create Engine
3. SQLAlchemy Automap Base
4. SQLAlchemy Reflect Tables
5. View Classes Found by Automap
6. Save References to Each Table
7. Create Session Link to the Database
8. Retrieve the Precipitation Data for a specified date range
9. Save Query Results and sort the DataFrame
10. Plot the Data
11. Generate the precipitation Summary
12. Find the Number of Stations and Determine the Most Active Stations for the specified date range
13. Find Low, High, and Average Temperatures from the list of active stations
14. Plot the Highest Number of Observations
15. Incorporate Flask into Data Analysis: Build Flask Routes
16. Set Up Flask and Create Routes
17. Set Up the Database and Flask: Set Up the Flask Weather App in VSCode
18. Set Up the Database
19. Set Up Flask
20. Create the Routes

## Initial Results
In the date range specified (August 2016 to October 2017), there were 9 active stations, the most active station with a count of 2272 records, recorded a maximum temperature of 85.0, a minumum temperature of 54.0, and an average temperature of 71.7. A histogram plot shows that the most ocurring temperature was around 76.0.
One trend we can observe based on the precipitation plot is that some months have higher amounts of precipitation than others. This plot provides insights around months where we would expect precipitation to be less and thus be a a good time for the surfing and ice-cream business.



![Precipitation_2016_2017](https://user-images.githubusercontent.com/67847583/122619578-5fec0400-d056-11eb-9f26-55effee23cfd.png)
![Temperature_Top_Station_2016_2017](https://user-images.githubusercontent.com/67847583/122619380-f2d86e80-d055-11eb-9b48-7bedb6fd199d.png)


## Results: June and December
Our temperarture summary statistics show that June typically has a higher mean temperature at 74.9 compared to December at 71.0.
Where 50% of the temperatures recorded for June were above 75.0, median temperature for December was 71.0
June has a minimum temperature of 64.0 while December has a minimum temperature of 56.0


#### June and December Summary Statistics
![June_Temps_Summary_Stats](https://user-images.githubusercontent.com/67847583/122620365-624f5d80-d058-11eb-94e6-e2ec1cf1c368.png)
![December_Temps_Summary_Stats](https://user-images.githubusercontent.com/67847583/122620371-667b7b00-d058-11eb-910c-71bc7509b12e.png)

#### Interpreting the June and December Temperature Results
Using a T-Test, we can detrmine if the mean temperature values are different for the two months. To do so, we have to define our Null and Alternate Hypothesis.
1. Null Hypothesis: µjune = µdecember (the means of both populations are equal)
2. Alternate Hypothesis: µjune ≠ µdecember (the means of both populations are not equal)

It is Important to note, we are specifying that the population does not have equal variance passing along False for the equal_var parameter. We know this because both samples were taken from populations (june and december) with different standard deviations.

Our T-Test show: P-Value:[4.19352984e-187] T-Statistic:[31.35503692]
We have a very small P-value to reject the Null Hypothesis. This means even though the standard deviations between our June and December are similar (3.257417, 3.745920), the difference in the population mean is statistically significant to consider the month of June and December different in terms of temperature.
