# Python API Project - What's the Weather Like?

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: _"Duh. It gets hotter..."_

But, if pressed, how would you **prove** it?

## Part I - WeatherPy

In this example, you'll be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

Your first objective is to build a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot add a sentence or too explaining what the code is and analyzing.

Your next objective is to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots explain what the linear regression is analyzing, any relationships you notice and any other analysis you may have.

Your final notebook must:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

### Observable Trends

* **Trend 1 -** Temperature vs Latitude Plot shows that the temperatures are higher the closer they are to the equator (latitude range of -20 to 20)

* **Trend 2 -** City Latitude vs Windspeed Plot shows that Windspeeds are somewhat indifferent to Latitudes, but it is important to note that highest wind speed outliers all occur at latitudes furthest from the equator.

* **Trend 3 -** Based on the data, it seems as though cloudiness and humidity are relatively consistent across all latitudes. Further analysis to include an additional variable may reveal further insights into those relationships

## Part II - VacationPy

Now let's use your skills in working with weather data to plan future vacations. Use Jupyter gmaps and the Google Places API for this part of the assignment.

* **Note:** if you having trouble displaying the maps try running `jupyter nbextension enable --py gmaps` in your environment and retry.

* Create a heat map that displays the humidity for every city from the part I of the homework.

  ![heatmap](Images/heatmap.png)

* Narrow down the DataFrame to find your ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.

  * **Note:** Feel free to adjust to your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number.

* Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

* Plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)

## To run the code:

To run these jupyter notebooks locally, you will need to obtain API keys.

* Install citypy in your python environment (https://pypi.python.org/pypi/citipy)

* For part one, you will need to obtain an API key for the OpenWeatherMap API, which can be obtained [here](https://home.openweathermap.org/api_keys).

* For part two, you wll need to obtain a Google API key from the Google Cloud Platform at <https://cloud.google.com> and enable the **Places API**.

* Get the API Keys and store them in the 'api_keys.py' file before running the Jupyter notebooks.
```python
# api_keys.py
weather_api_key = 'API_KEY_HERE'
g_key = 'API_KEY_HERE'
```
### Copyright

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Trilogy Education Services © 2019. All Rights Reserved.
