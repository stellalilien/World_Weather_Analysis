# World Weather Analysis

## Project Overview

The purpose of this project was to develop a product that allows users to input their vacation weather preferences which can then be used to identify matching travel destinations and nearby hotel accomodations. As an example a set of four cities meeting the input criteria are chosen to create an itinerary and a travel route using Google Maps Directions API.

## Weather Data

In order to create the weather database needed the first necessary step was to populate enough random combinations of latitudes and longitudes and then use the citipy module to identify the nearest cities to each set of coordinates.

<img width="295" alt="image" src="https://user-images.githubusercontent.com/94754972/152705506-e7d441f2-cb17-49d3-8356-517744509f21.png">

Once those cities have been identified and stored in a list the next step is to make an API request for each city in the list in order to gather the necessary weather data.

<img width="294" alt="image" src="https://user-images.githubusercontent.com/94754972/152705638-60f88f1e-9d19-4788-8c81-68b04fd48fdd.png">

All of the data retrieved from the API requests was then stored in a DataFrame.

<img width="364" alt="image" src="https://user-images.githubusercontent.com/94754972/152705699-c9ab96b3-0b34-44f9-a2d9-5061e8a48c15.png">


## Travel Destination Map

Once the DataFrame containing all of the city data has been created the user input was used as a filter and a new DataFrame was created to reflect cities that meet those requirements. 

<img width="371" alt="image" src="https://user-images.githubusercontent.com/94754972/152705985-8c5b9f76-2bee-4b60-a9c3-e0920b59c118.png">

Those cities were then used in a Google API request to collect data on hotel accomodations in the provided cities.

<img width="377" alt="image" src="https://user-images.githubusercontent.com/94754972/152706101-0f5a6ae8-ef25-4a33-8844-8e9de287e9c6.png">

<img width="286" alt="image" src="https://user-images.githubusercontent.com/94754972/152706136-411587c4-a051-4cb3-a5e2-a9a37c46c902.png">

## Travel Itinerary Map

Using the previous map four cities were chosen and the coordinates were extracted from the DataFrame.

<img width="390" alt="image" src="https://user-images.githubusercontent.com/94754972/152706328-ca576b36-8570-42b3-89a9-c59e6b7e4b0a.png">

Those cities were then used to create a vacation itinerary driving map.

<img width="195" alt="image" src="https://user-images.githubusercontent.com/94754972/152706398-6139acf0-2b7c-47ce-836c-dc822fc80579.png">

A second map was then created with markers indicating the hotel information for each of the cities on the itinerary.

![WeatherPy_travel_map_markers](https://user-images.githubusercontent.com/94754972/152706444-50097ad0-20cd-4f29-b498-b8914eccbad3.png)
