# NYC Uber Trip Visualization

- Link to the Tableau Public:
https://public.tableau.com/profile/max.zhao2915#!/vizhome/UberNYC_16175917883130/1_1



### Dataset Description

1. Uber trip raw data from 2014(April-September). The files are separeted by month ans each has the folling columns:
 - Date/Time : The date and time of the Uber pickup
 - Lat : The latitude of the Uber pickup
 - Lon : The longitude of the Uber pickup
 - Base : The TLC(y Taxi and Limousine Commission) base company code affiliated with the Uber pickup
2. NY Weather Data from 2014(Apr'14-July'14) with the folling columns:
 - Date
 - Temp. (°C)high
 - Temp. (°C) avg
 - Temp. (°C) low
 - Dew Point (°C) high
 - Dew Point (°C) avg
 - Dew Point (°C) low
 - Humidity (%) high
 - Humidity (%) avg
 - Humidity (%)low
 - Sea Level Press. (hPa)high
 - Sea Level Press. (hPa)avg
 - Sea Level Press. (hPa)low
 - Visibility (km)high
 - Visibility (km)avg
 - Visibility (km)low
 - Wind (km/h)high
 - Wind (km/h)avg
 - Wind (km/h)low
 - Precip. (mm)sum
 - Event


### Data Preparation
The original data contains one Excel file with the weather infomation and 4 months of Uber pickups'data.
The first step is to import data into Python and using Pandas to convert it into the standard format. For example: load the data as 'str' data type first, then use'pd.to_datetime' and 'dt.strftime('%Y/%m/%d')' to convert date data into 'yyyy/mm/dd'
![Screen Shot 2021-04-05 at 5 20 24 PM](https://user-images.githubusercontent.com/69823722/113733726-bdfc8280-96c8-11eb-96a2-8f3852cd248b.png)

After that, combined the Uber trips data for four month into one dataframe with 'pd.concat'. It also can be done by the new version of Tableau using the 'Edit Relationship'![Screen Shot 2021-04-06 at 11 22 31 AM](https://user-images.githubusercontent.com/69823722/113735870-a32b0d80-96ca-11eb-8e06-b844c734920b.png)

Then, the tables with Uber trip and weather data should be joined together based on the same date for analysis.

### Data Visualization and Analysis
Dashboard
![Screen Shot 2021-04-06 at 11 18 46 AM](https://user-images.githubusercontent.com/69823722/113735123-f2247300-96c9-11eb-82d8-41f8d4f9bec6.png)
Link:https://public.tableau.com/profile/max.zhao2915#!/vizhome/UberNYC_16175917883130/1_1

- According to the map which displays the distribution of rides gepgraphically, we will find that the most of the Uber trips take place in Manhatten which is the most densely populated of New York City's 5 boroughs, and B02512 is the most affiliated code in this area.
- A histogram to display the rides distribution among hours of the day. It shows that a large part of people in these areas working in the Manhattan and during the rush hour, people frequently call Uber for transportation on workdays.
- On the contrary, during the weekends, people usually won't go out in the morning. There is a traffic peak at around 4pm, which means people tend to have more night lives during the weekends than the workdays.
- The weekday trip number trend in different month and compare with the various weather conditions. It give infomation that the most two important factors affecting the Uber trips number are the precipitation and the average wind speed.
- People would like to take more Uber trips from Tuesday to Friday
  

