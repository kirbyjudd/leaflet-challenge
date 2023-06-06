# leaflet-challenge Module 15 Challenge

## Background
The United States Geological Survey, or USGS for short, is responsible for providing scientific data about natural hazards, the health of our ecosystems and environment, and the impacts of climate and land-use change. Their scientists develop new methods and tools to supply timely, relevant, and useful information about the Earth and its processes.

The USGS is interested in building a new set of tools that will allow them to visualize their earthquake data. They collect a massive amount of data from all over the world each day, but they lack a meaningful way of displaying it. In this challenge, you have been tasked with developing a way to visualize USGS data that will allow them to better educate the public and other government organizations (and hopefully secure more funding) on issues facing our planet.

## Part 1: Create the Earthquake Visualization
For this leaflet challenge I utilized the openstreetmap.org tile for my tile layer and then set the api queryURL to the most recent earthquake week geojson data (https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_week.geojson).

I then used the D3 JS library to perform a get request to the query URL to retrieve the: lattude, longitude, depth, magnitude, and location of the most recent weeks earthquakes.

I created a function called 'depthColor' that used if conditionals to return a specific color. 
- 90+ return red
- 50-70 return orange
- 30-50 return yellow
- 10-30 return yellowgreen
- -10-10 return lawngreen

I then created a circle marker that took in the latitude and longitude, set the fill color the the depthColor function, and se the radius to the magnitude valueus * 20000.

AFter adding the circle marker to myMap I attached a bindPopup that displayed the Magnitude, location and depth of the earthquake.

Lastly I added a legend to myMap that displays the depth limits and its corresponding circle color.

## Peer Cooperation
I worked together on this assignment with my classmate Riddhi Sodagar.

## File Locations
The logic.js code file is located 'Leaflet-Part1'/'static' in the 'js' folder.

The index.html is located in 'Leaflet-Part1' folder.
