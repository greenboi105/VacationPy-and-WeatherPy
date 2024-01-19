# Utilizing Weather and Map APIs for Geographical Visualization

Source code is found in the visualization_notebooks folder with the respective notebook names WeatherPy and VacationPy.

## WeatherPy

1. We first generate pairs of random geographical coordinates (latitude and longitude) to input the pair into the citipy module to determine the nearest city. This in turn generates a random list of cities across the world.

2. We then contact the OpenWeatherMap API to extract the weather data for each random city. We append the weather data to a list in the form of a dictionary. This list of dictionaries can then be converted to a pandas DataFrame for easier handling.

3. The next step is to plot relationships between geographical characteristics and physical characteristics of the cities.

    - The first plot demonstrates that cities closest to a latitude of zero (cities closest to the equator) are the warmest.

    - The second plot discovers no immediate relationship between the latitude of a city and the humidity of a city. It is more likely that other geographical characteristics such as the local terrain more directly influence the humidity of a city.

    - Similarly, the third plot demonstrates no direct relationship between latitude and cloudiness.

    - Wind speed is also not directly related to latitude.

4. We finally want to determine a line of best fit between the relationships of northern and southern cities. We first split the DataFrame into northern and southern cities.

    - For the first plot between temperature and latitude, the relationship is either positively correlated or negatively correlated depending on whether the city is northern or southern. A northern city will have a negative correlation due to increasing distance from the equator, while a southern city will have a positive correlation due to decereasing distance from the equator.

    - There is not a particularly strong relationship between humidity and latitude again.

    - The larger coefficient for the southern hemisphere indicates that cities closer to the equator are generally cloudier than those further from the equator in the southern hemisphere.

    - Windiness is again not a feature that is strongly influenced by the distance from the equator, and is more likely influence by other local geographical factors.

## VacationPy

1. We have a list of cities from the WeatherPy portion, and we can now filter the cities for desirable weather and determine the nearest hotel to each city.

2. We first filter the city data with our desired conditions.

3. We then utilize the geoapify API to find the nearest hotel to each city and construct a DataFrame with the characteristics of each city along with the associated hotel.

4. Finally, we can plot the cities and corresponding hotels to see where we can find our desired weather characteristics.

Link to VacationPy Visualizations: [Link to Google Colab](https://colab.research.google.com/drive/10GGCooa91jOwf_QK2fxnwiCJNwH-hMbh#scrollTo=0GLaPmAzlPDI)
