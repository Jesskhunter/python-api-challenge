# Python API Challenge - What's the Weather Like?

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: "Duh. It gets hotter..."

But, if pressed, how would you prove it?

## Part I - WeatherPy
In this example, you'll be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.

The first requirement is to create a series of scatter plots to showcase the following relationships:

Temperature (F) vs. Latitude
Humidity (%) vs. Latitude
Cloudiness (%) vs. Latitude
Wind Speed (mph) vs. Latitude
After each plot, add a sentence or two explaining what the code is analyzing.

The second requirement is to run linear regression on each relationship. This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

Northern Hemisphere - Temperature (F) vs. Latitude
Southern Hemisphere - Temperature (F) vs. Latitude
Northern Hemisphere - Humidity (%) vs. Latitude
Southern Hemisphere - Humidity (%) vs. Latitude
Northern Hemisphere - Cloudiness (%) vs. Latitude
Southern Hemisphere - Cloudiness (%) vs. Latitude
Northern Hemisphere - Wind Speed (mph) vs. Latitude
Southern Hemisphere - Wind Speed (mph) vs. Latitude
After each pair of plots, take the time to explain what the linear regression is modeling. For example, describe any relationships you notice and any other analysis you may have.

Your final notebook must:

Randomly select at least 500 unique (non-repeat) cities based on latitude and longitude.
Perform a weather check on each of the cities using a series of successive API calls.
Include a print log of each city as it's being processed with the city number and city name.
Save a CSV of all retrieved data and a PNG image for each scatter plot.

## Part I Observed Trends:

-There is a strong correlation between latitude and temperature. In this data set, analyzed in May, you can see that most of the "hot spots" are located between the Tropic of Cancer (latitude 23.5° N) and the Tropic of Capricorn (latitude 23.5° S) with the Eqautor directly in the middle at 0°. Since it is a transitory period (the NH is approaching summer and the SH is approaching winter) there are also outliers. 

-There appears to be no correlation between latitude and humidity. Both the NH and SH have a large variance of percentages from around 10 to 100.

-There appears to be no correlation between latitude and wind speed. Both the NH and SH have a large variance of speeds from around 10 to 100.

-The correlation between latitude and cloudiness is not pronounced, however, a large portion of the data points are gathered at both 0 and 100.



## Part II - VacationPy
Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part of the assignment.

Create a heat map that displays the humidity for every city from Part I.

![heatmap](https://user-images.githubusercontent.com/75280556/118706406-52d5be00-b7e7-11eb-8702-bc7a8c7296e7.png)

![heatmapsatellite](https://user-images.githubusercontent.com/75280556/118706375-4c474680-b7e7-11eb-8a99-d4e31e84e434.png)

Narrow down the DataFrame to find your ideal weather condition. For example:

A max temperature lower than 80 degrees but higher than 70.

Wind speed less than 10 mph.

Zero cloudiness.

Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.

Note: Feel free to adjust to your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number.

Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

Plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.


![hotelmap](https://user-images.githubusercontent.com/75280556/118706400-51a49100-b7e7-11eb-9743-ecf373ba097a.png)

![hotelmapsatellite](https://user-images.githubusercontent.com/75280556/118706389-4f423700-b7e7-11eb-809b-1985ff18ff4a.png)


