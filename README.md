# World_Weather_Analysis

## Module 6 Challenge ~ WeatherPy with Python APIs
---
## Overview of Project
- After helping Jack with the PlanMyTrip app, he and Beta testers loved it and recommended a few changes to take the app to the next level. Specifically, they suggested adding the weather description to the weather data you’ve already retrieved. In a new version of PlanMyTrip App, input statements would inquire the beta testers to filter the data for their personal weather preferences, which will then be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, the beta tester will choose four different cities to create a personal travel itinerary. Lastly, using the Google Maps Directions API, the app will create a travel route between the four cities as well as a marker layer map.
### Purpose
- In this module, we practice our analysis, visualization, and statistical skills by retrieving and analyzing weather data for a hypothetical travel company, PlanMyTrip. 
1. In this challenge, we performed task using new Python libraries and modules (Pandas, gmaps, requests, numpy, random, matplotlib, timeit, scipy, citipy, datetime, time)
2. Retrieve and use data from an API "get" request to a server.
3. Retrieve and store values from a JSON array.
4. Use try and except blocks to resolve errors.
5. Write Python functions.
6. Create scatter plots using the Matplotlib library, and apply styles and features to a plot.
7. Perform linear regression, and add regression lines to scatter plots.
8. Create heatmaps, and add markers using the Google Maps API.
---
### Results: 
**Deliverable 1 ~ Retrieve Weather Data**
- I refactored the WeatherPy notebook to build a bigger Weather Database and retrieve a 2,000 sets of random latitudes and longitudes. The set is stored in a list of cities, then parsed using JSON format, then converted into a pandas dataframe. 
- I performed an API call with the OpenWeatherMap to get the nearest city's latitude & longitude, maximum temperature, percent humidity, percent cloudiness, wind speed, and weather description (for example, clouds, fog, light rain, clear sky).
![Weather_Database](https://user-images.githubusercontent.com/68654746/178605929-bf300e80-1ada-4a5b-8c33-0792ff0d4525.png)

**Deliverable 2 ~ Create a Customer Travel Destinations Map**
- A travel destinations map is created by reading the weather database file into a dataframe, prompting the user to enter minimum and maximum temperature criteria, and filtering the dataframe based on the user weather preferences while creating a new dataframe out of the filtered information. Then a new dataframe is created by adding a column for nearby hotels. Nearby hotels are found by using a Google Maps & Places API Key to search for hotels within 5,000 meters of the random coordinates in the weather database. A marker layer is added for the hotel names and the information is displayed as a destination map.
![WeatherPy_vacation_map](https://user-images.githubusercontent.com/68654746/178606378-8330bbd9-55c8-427e-aced-55459b296ad9.png)

**Deliverable 3**
- Using the Google Directions API key, the PlanMyTrip app will create a personal travel itinerary that shows the route between the four cities chosen from the customer’s possible travel destinations. The last part of the application updates, I created a marker layer map with a pop-up marker for each city on the itinerary. The updated PlanMyTrip app now allows users to plan a temperature-preferenced based map itinerary for their next upsoming trip!
#### Travel Map
![WeatherPy_travel_map](https://user-images.githubusercontent.com/68654746/178606623-2c67a114-3802-406e-aae1-e57a5a543219.png)

#### Travel Map with Markers for each hotel showing Current Weather Descriptions
![WeatherPy_travel_map_markers](https://user-images.githubusercontent.com/68654746/178606677-9fb8010a-747f-40be-a67a-a2eea158f2c5.png)
