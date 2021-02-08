# IBM CAPSTONE PROJECT 
### Battle of the neighborhoods – building a hotel in Queens New York 
<img src="Queens bridge Cropped.jpg">

#### This project uses data science to determine the optimum Queens neighborhood to build a hotel that can be an alternative for business travelers who can’t afford the more expensive hotels in Manhattan  

## A. Introduction
### A.1 Background 
In New York city, the borough of Manhattan is an important location for many groups of people. It is the financial hub for thousands of business travelers and a prime destination for the millions of tourists traveling to the city annually. As a result of this, hotel cost in Manhattan can be very expensive compared to the neighboring boroughs. To alleviate this problem for travelers, one option is for hotel companies to build hotels in the less expensive neighboring boroughs of Queens, Brooklyn or the Bronx. Travelers can book hotels in the neighboring boroughs and then commute to Manhattan. Since Manhattan is where most travelers will do business or vacation, it is important for them to book hotels close to Manhattan to reduce the daily travel time and cost. For a hotel chain, knowing the optimal neighborhood within a neighboring borough to build the hotel is key to solving these problems. Knowing the right neighborhood to build the hotel can reduce booking cost, travel time and travel cost for their Manhattan bound customers. In addition, knowing the number of existing hotels within the neighborhood can also minimize competition from other hotel chains. In this project we will focus on finding the optimal neighborhood in the borough of Queens. 

### A.2 Business Problem
The purpose of this project is to find the optimal neighborhood in Queens New York to build a hotel for Manhattan bound travelers who can’t afford the more expensive hotels in Manhattan. More specifically the analysis determines the closest Queens neighborhood to Manhattan with the lowest number of existing hotels. The results from this report can be used as reference for hotel stakeholders interested in building a hotel in Queens for Manhattan bound travelers. 


## B. Data Acquisition & Exploration 

### B.1 Data Acquisition  
To solve this problem, we need to find the neighborhood that’s closest to mid-town Manhattan with the minimum number of hotels. This involves acquiring data on neighborhoods and hotels in New York city. More specifically location data on all neighborhoods in the borough of Queens and the total number of hotels in each neighborhood. I was able obtain data from two locations.  

Location data and hotel data was acquired from the following two locations:

•	Neighborhood data was acquired from the NYU university website https://geo.nyu.edu/catalog/nyu_2451_34572 

•	Hotel data was acquired from the Four-Square location and venue platform www.foursquare.com 

### B.2 Data Exploration & Cleaning
The neighborhood data downloaded from the NYU website comes in JSON format and has the coordinates of all neighborhoods in all five boroughs in New York city. Since our focus is on the boroughs of Queens and Manhattan, the original dataset was cleaned and reduced to just the neighborhoods in Queens. The following data frame consisting of the Borough, Neighborhood, Latitude and Longitude was created.

<img src="Queens_Neighborhood table.JPG" width=400>

The hotel data for each Queens neighborhood was obtained from the Four-Square location platform using the coordinates of each neighborhood. A data frame consisting of the hotels in each Queens neighborhood was created  

<img src="Queens_hotel table.JPG" width=200>

## C. Methodology  
As previously mentioned, our goal is to find the neighborhood that’s closest to mid-town Manhattan with the minimum number of hotels. In the section above we acquired and cleaned the necessary data needed to accomplish this goal. In this section I applied various data science techniques and methods to the data to determine the optimum Queens neighborhood. The following task was performed. 

•	I used the Python Folium map library to visualize and analyze the layout of the Queens neighborhoods relative to midtown Manhattan.   

•	I used the Python Folium map library to visualize and analyze the layout of the Queens hotels relative to midtown Manhattan 

•	Use Matplotlib to create bar charts of the hotels in each Queens neighborhoods for more analysis

•	Use the Haversine formula to calculate the distance from each Queens neighborhood to mid-town Manhattan. This distance data was added to the final feature set for clustering 

•	Combine and normalize all relevant features for clustering 

•	Apply K-means clustering method to the feature set 

•	Use the Python Folium map library to the visualize and analyze the clusters 

### C.1 Data Visualization 

Now let visualize and analyze the map of Queens neighborhoods

<img src="Map of Queens Neighborhoods.JPG" width=400>

