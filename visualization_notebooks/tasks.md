# Tasks

We want to combine what we have learned about requests, APIs, and JSON to answer the question of what the weather is like as we approach the equator.

## Part 1: WeatherPy

Here we want to create a Python script to visualize the weather of 500 cities of different distances from the equator.

### Task 1: Creating Plots to Showcase the Relationship Between Weather Variables and Latitude

We use the OpenWeatherMap API to retrieve the weather data from the cities list generated in the starter code.

We then create a series of scatterplots to display the relationships:

- Latitude vs. Temperature

- Latitude vs. Humidity

- Latitude vs. Cloudiness

- Latitude vs. Wind Speed

### Task 2: Compute Linear Regression for Each Relationship

Secondly, we compute the linear regression for the different relationships. We separate the plots into Northern Hemisphere and Southern Hemisphere.

We then create a series of scatter plots, including the linear regression line, the model's formula, and the r values.

## Part 2: VacationPy

We want to use the weather data to plan future vacations.

To create the map visualizations, we follow the steps below:

- Create a map that displays a point for every city in the city_data_df DataFrame. The size of the point is the humidity in the city.

- We narrow down the city_data_df DataFrame to find the ideal weather condition.

- Create a new DataFrame called hotel_df to store the city, country, coordinates and humidity.

- For each city use the Geoapify API to find the first hotel located within 10,000 meters of the coordinates.

- Add the hotel name and the county as additional information in the message for each city on the map.
