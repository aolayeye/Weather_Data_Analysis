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
In the date range specified (August 2016 to October 2017), there were 9 active stations, the most active station with a count of 2272 records, recorded a maximum temperature of 85.0, a minumum temperature of 54.0, and an average temperature of 71.7. A histogram plot shows that the most ocurring temperature was around 75.0. 


![Precipitation_2016_2017](https://user-images.githubusercontent.com/67847583/122619136-5e6e0c00-d055-11eb-965a-e72ea3e8ea71.png)
![Temperature_Top_Station_2016_2017](https://user-images.githubusercontent.com/67847583/122619380-f2d86e80-d055-11eb-9b48-7bedb6fd199d.png)







