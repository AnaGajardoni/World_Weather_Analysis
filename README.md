# World_Weather_Analysis
Analysis on weather-information (temperature, humidity, cloudiness, etc) of a random set of points in the globe (latitude/longitude) and pointing places on a map based on latitude/longitude geo positions.

## Purpose
The purpose of this project is to obtain weather data through API's using Python, treat it and create heat maps and itineraries using google maps library. There were many steps to reach the final deliverables and they will be listed below.

Use of api_keys to connect to sites

### Deliverable 1: Deliverable 1: Retrieve Weather Data
- Use of numpy library to generate a set of 2000 latitude/longitude pairs;
- Use of citipy library to retrieve city information based on latitude/longitude;
- Use of pandas library to create a data frame to store city information: City, Country, Latitude, Longitude, Maximum Temperature, Humidity, Cloudiness, Wind Speed and General Weather Description;
- Creation of output file (csv) with the data listed in the previous step.

### Deliverable 2: Create a Customer Travel Destinations Map
- Use of data from Deliverable 1 as input for searches;
- Data filtering based on user input (minimum/maximum desired temperatures);
- Find closest hotel for a given latitude/longitude pair using google Directions API - parsing JSON data returned by requests call;
- Creation of heat map (gmaps) using filtered data with added marker layer pointing information on each location such as: hotel name, city, country and current weather;
- Creation of output file (csv) with the data listed in the previous steps (filtered data and hotel information).

### Deliverable 3: Create a Travel Itinerary Map
- Use of data from Deliverable 2 as input;
- Creation of map with markers for all locations;
- Creation of map (gmaps) with itinerary based on four selected points (the fifth is actually the starting point since the idea is to make the trip end at the same point it started).

## Final Considerations
This was a complex project because the steps involved using different python libraries and techniques. I would list the following two as the most important ones:
- Making API calls and parsing JSON data: this was not difficult, but it is extremely important since lots of data can be acquired this way. Parsing retrieved data was a good exercise to get familiar with the kinds of formats we can find as a result of such calls.
- Using gmaps library - even if simple calls - gave me a good hint not only of what can be done with gmaps, but also of what kind of documentation is available for API's like this.