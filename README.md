# python-api-challenge
Module 06 WeatherPy API Challenge

Overview
===

The goal of this challenge is to use Python and API keys to request information and perform JSON functions to gather data and answer the question: "What is the weather like as we approach the equator?" There are two parts in challenge:
1. WeatherPy - use Python to visualize the weather of 500+ cities (based on their distance from the equator) by pulling data from OpenWeatherMap API and the citipy Python library.
2. VacationPy - use Python to plan a vacation by pulling data from Geoapify API and the geoViews Python library.

***********
### Part  1: WeatherPy

#### Requirement 1
* Use OpenWeatherMap API to get weather data from the cities list in starter code.

This part of the challenge required using the OpenWeatherMap API to request and process weather data to find relationships between latitudes and various weather conditions (specifically temperature, humidity, cloudiness, and wind speed.

To start, cities were randomly generated from the citipy library then fed into OpenWeatherMap API to request and respond their coordinates, maximum temperatures, humidity, cloudiness, wind speeds, and country into a JSON format. This data was then used to create a Pandas dataframe where all elements could be easily referenced for plots, as well as saved to a CSV.

Next, scatter plots were created to show the following relationships:
   - latitude vs temp
   - latitude vs humidity
   - latitude vs cloudiness
   - latitude vs wind speed
   
In this section, the northern hemisphere (NH) and southern hemisphere (SH) were not taken into consideration separately. The most prominent graph, Latitude vs Temperature (All Cities), shows a clear relationship between latitude and temperature, with higher temperatures being more closely concentrated around the equator and decreasing as latitude increases or decreases (see cell 10 in Jupyter Notebook). The points create a distinct parabolic shape.

The remaining plots show that latitude/distance from the equator and the weather conditions were far less concentrated around any specific area, suggesting that latitude has less effect on humidity, cloudiness, and wind speed, unless other factors are taken into consideration (such as bodies of water or landmasses).
   
#### Requirement 2
* Compute linear regression for each relationship. Separate the plots into northern hemisphere (NH, >=0 deg lat) and southern hemisphere (SH, <0 deg lat). Define a function to calculate linear regression for each set of relationships.

First, a function to find the linear regression of each relationship was defined. It is coded in such a way that the function becomes a simple callout in each set of relationships (instead of typing it out every time and creating clutter in the notebook). The function includes variables for finding the slope, y-intercept, r-value, p-value, and standard error and applying them to create the scatter plots.

The function also configures various aspects of the plots, such as x- and y-labels, titles, color of the points, and placing the line equation on each plot. In addition, the funtion also prints the regress values, line equation, and r-value with the scatter plots.

The next step was to create separate dataframes for the NH and SH, simply by filtering the latitudes for greater than/equal to 0 (NH) and less than 0 (SH).

The following plots were created to showcase relationships between:
   -NH: temp vs latitude
   -SH: temp vs latitude
   
   -NH: humidity vs latitude
   -SH: humidity vs latitude
   
   -NH: cloudiness vs latitude
   -SH: cloudiness vs latitude
   
   -NH: wind speed vs latitude
   -SH: wind spped vs latitude
   
In general, as was demonstrated in the first requirement, there is a more distinct relationship between latitude and temperature than latitude and the other weather conditions. It is likely that more variables (such as distance to bodies of water, land masses, time of year, etc.) would need to be included to draw better conclusions about how latitude affects certain weather conditions.
   
   
*************
### Part 2: VacationPy
* Use geoViews and Geoapify API to take the list of cities generated in WeatherPy and narrow down vacation destinations by ideal weather conditions, as well as find hotels.

First the city data from WeatherPy was imported and put into a dataframe to access the city information at a glance. Next a world map was generated with hvplot and displays the cities as points. The size of each point is determined by the humidity data from the dataframe.

Next the weather conditions were wittled down by defining specific ranges for each, based on the coder's preferences, and any null values were dropped.

Once the ideal conditions were filtered, a new data frame was created with an empty column to display hotel names for each city. The hotel column was populated by sending a request to Geoapify API with parameters for limits, radius (in meters), categories (hotels), and the city coordinates for each row. Once the data was retrieved, the results were stored in the hotel dataframe.

Finally, a new plot was configured showing only the cities that met the ideal conditions, with the added benefit of adding the city's country and hotel information in the hover tool.

### Sources
In this challege I relied heavily on the Xpert Learning Assistant tool, tutoring, office hours, and activities from Module 6 to complete the assignment.
