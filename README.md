# Rideshare Analysis
Analyzing data for a potential ridesharing app and present data and visualizations to the mock client. This assignment was a part of UC Berkeley's Data Analytics Bootcamp.

## Data
City and ride data were provided in CSV files.

## Project
 In this challenge, I used city data and rider data to create a data frame showing all the data by the type of city- rural, suburban or urban. The analysis shows that the Pyber ride share company is overwhelming used in urban cities compared to suburban and rural cities but the average fare for rural cities is significantly higher. The low number of drivers and higher average fares in the rural cities have also led to much higher average fares per driver. It is almost $40 more for drivers in rural cities versus drivers in urban cities. Please see the table and chart below. 

|          |   Total Rides |   Total Drivers | Total Fares   | Average Fare per Ride   | Average Fare per Driver   |
|:---------|--------------:|----------------:|:--------------|:------------------------|:--------------------------|
| Rural    |           125 |              78 | $4,327.93     | $34.62                  | $55.49                    |
| Suburban |           625 |             490 | $19,356.33    | $30.97                  | $39.50                    |
| Urban    |          1625 |            2405 | $39,854.38    | $24.53                  | $16.57                    |

![Fares by City type](/images/Total_Fares_by_City_Type.png)

In the challenge analysis, I encountered difficulties setting the index to the datetime format to properly move the data into a pivot table. Properly renaming the new dataframe and making sure that the data column was replacing the previous index by using `inplace=true` in the `.set_index` function produced the result I was hoping for. This allowed the subsequent analysis to be properly rooted with the date index.  

Based on the available data and analysis, increasing the number of drivers in rural cities could increase the total number of rides in those cities and bring the total fare up. The same can be done in the suburban cities as there is almost 40% the number of drivers there compared to urban cities. Before adding additional drivers, I would analyze the average distance of the rides given and look to see if any rides were declined due to lack of drivers. For analyzing the average distance of the ride, I would perform similar steps to looking at the average fare and calculate the averages by city type. To analyze the demand, I would look at the number of ride requests met versus the number of ride requests declined and group them by city type as well. 

## Tech Used
- Python 3.7.3
- Jupyter Notebooks
- Matplotlib
- NumPy
- SciPy
- Pandas

#### Sample Code
![Rideshare Code](/images/Rideshare_code.png)