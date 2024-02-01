# python-api-challenge
Module 06 WeatherPy API Challenge

Overview
===

The goal of this challenge is to use Python and API keys to request information and perform JSON functions to gather data and answer the question: "What is the weather like as we approach the equator?" There are two parts in challenge:
1. WeatherPy - use Python to visualize the weather of 500+ cities (based on their distance from the equator) by pulling data from OpenWeatherMap API and the citipy Python library.
2. VacationPy - use Python to plan a vacation by pulling data from Geoapify API and the geoViews Python library.

***********
### Part  1: WeatherPy
REMEMBER TO CHECK THE HINTS/CONSIDERATIONS ON THE CHALLENGE PAGE
Requirement 1
-use OpenWeatherMap API to get weather data from the cities list in starter code.
-scatter plots for the following relationships:
   -latitude vs temp
   -lat vs humidity
   -lat vs cloudiness
   -lat vs wind speed
   
Requirement 2
-compute linear regression for each relationship. separate the plots into Northern Hemi (NH, >=0 deg lat) and Southern Hemi (SH, <0 deg lat). define a fcn to to create the linear regr plots.
-create a series of scatter plots. include linear regr line, model's formula, and r values (see pic in challenge page).
-create the following plots:
   -NH: temp vs lat
   -SH: temp vs lat
   
   -NH: humidity vs lat
   -SH: humidity vs lat
   
   -NH: cloudiness vs lat
   -SH: cloudiness vs lat
   
   -NH: wind speed vs lat
   -SH: wind spped vs lat
   
   -*after each pair of plots, explain what the linear regr is modeling. describe any relationships you notice and any other findings*
   
### GRADING REQUIREMENTS
#### PLOTS TO SHOW RELATIONSHIP B/T WEATHER VARS AND LAT
-Use the OpenWeatherMap API to retrieve weather data from the cities list generated in the started code (10 points)

-Create a scatter plot to showcase the relationship between Latitude vs. Temperature (5 points)

-Create a scatter plot to showcase the relationship between Latitude vs. Humidity (5 points)

-Create a scatter plot to showcase the relationship between Latitude vs. Cloudiness (5 points)

-Create a scatter plot to showcase the relationship between Latitude vs. Wind Speed (5 points)

#### LINEAR REGR FOR EACH RELATIONSHIP
-Linear regression scatter plot for Northern Hemisphere: Temperature (C) vs. Latitude (5 points)

-Linear regression scatter plot for Southern Hemisphere: Temperature (C) vs. Latitude (5 points)

-Linear regression scatter plot for Northern Hemisphere: Humidity (%) vs. Latitude (5 points)

-Linear regression scatter plot for Southern Hemisphere: Humidity (%) vs. Latitude (5 points)

-Linear regression scatter plot for Northern Hemisphere: Cloudiness (%) vs. Latitude (5 points)

-Linear regression scatter plot for Southern Hemisphere: Cloudiness (%) vs. Latitude (5 points)

-Linear regression scatter plot for Northern Hemisphere: Wind Speed (m/s) vs. Latitude (5 points)

-Linear regression scatter plot for Southern Hemisphere: Wind Speed (m/s) vs. Latitude (5 points)
   
*************
### Part 2: VacationPy
REMEMBER TO CHECK THE HINTS/CONSIDERATIONS ON THE CHALLENGE PAGE
*reference the images on the challenge page*

1. create a map that displays a point for every city in the city_data_df. the size of the point should be the humidity in each city.

2. narrow down city_data_df to find your ideal weather condition (such as: max temp 21<max temp<27 deg, wind speed <4.5 m/s, zero cloudiness, etm.). adjust specs as you like but have a reasonable limit to the number of rows your API requests return.

3. create new df hotel_df to store the city, country, coordinates, and humidity.

4. for each city, use Geoapify API to find first hotel located within 10,000 m of your coordinates.

5. add hotel name and the country as add'l info in the hover message for each city on the map.
   
### GRADING REQUIREMENTS
-Create a map that displays a point for every city in the city_data_df DataFrame (5 points)

-Narrow down the city_data_df DataFrame to find your ideal weather condition (5 points)

-For each city in the hotel_df DataFrame, use the Geoapify API to find the first hotel located within 10,000 metres of your coordinates (10 points)

-Add the hotel name and the country as additional information in the hover message for each city in the map. (10 points)

