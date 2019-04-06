# Full Report on the Capstone

## Sections:

__1. Introduction__\
__2. Data Description__\
__3. Methodology__\
__4. Results__\
__5. Discussions__\
__6. Conclusion__

## Introduction

__Identifing the popular food cuisines in the top cities of India as well as to identify the similarities between the food cuisines of these cities.__\
How does the types of cuisines in India vary? Are the Indian cuisines more popular in the top cities of India or any other cuisines are popular in the cities of India? These are a few of the questions to be answered in the notebook. We shall dive deep into the location data and data from Foursquare. This can help us to understand the popular food cuisins in a particular city as well as the similarities between the food cuisines of these this would help the people who are looking to start buinesses like restaurants by providing the information of the food cuisines of the city in which they are setting up the restaurant and also help the top restaurant brands that run a chain of restaurants by providing the similarities in the food cuisines of the cities.

## Data Description

__India Cities Dataset__\
The cities are ranked based on the population of the city. The population data is taken from [here](https://en.wikipedia.org/wiki/List_of_cities_in_India_by_population#1_to_25).
From the wikipedia page the following data is scraped that contains the following features.
1.City :- Contains the name of the City.\
2.Population :- Contains the population of the City.\
3.State:- To which State does the City belongs to.
Then with the help of geolocater the geospatial coordinates of the cities will be calculated.

## Methodology

This notebook follows the following Methodology:\
1.Collecting the data\
2.Cleaning the data\
3.Visualization\
4.Machine Learning

__Step 1: Collecting Data__\
The datasets used in this notebook are collected from Wikipedia. Please refer to the Data Description section for more information about the data.
The Foursquare data, will be added within the notebook and no external file will be created for it. The API calls will be made within the 
code cell. Once the necessary data is collected, cleaning the data is done.

__Step 2: Cleaning Data__\
There is not much of data cleaning done here as the data was scraped from the wikipedia page and the coordinates are calculated with the help of
geolocater. The city named Gaziabad is removed from the data as Foursquare API was not able to process it.The final datset is available [here](https://github.com/Gautham000/Coursera_Capstone/blob/master/Final%20capstone/India%20city%20locations.csv).

__Step 3: Visualization__\
A few simple visualizations are made in order to get a better understanding of the data. Folium is used for this purpose. Folium generates 
interactive and beautiful maps, using the Latitude and Longitude we provide. The folium visualizations will be made available in the 
comments section.
Further to enhance the understanding of the data, count plots are used to better understand the final result.

__Step 4: Machine Learning__\
KMeans clustering algorithm is used on the most common venues dataframe to identify the probable clusters for different types of restaurants.
we have initialized 4 clusters for the dataset.

## Results
1.Indian restaurants are the 1st most popular preferred type of food in the indian cities.\
2.Sount Indian restaurants along with Fast food restaurants are the 2nd most popularly preferred type of food in the indian cities.\
3.The cities 'Agra', 'Ahmedabad', 'Bhopal', 'Delhi', 'Nagpur', 'Nashik', 'Pimpri-Chinchwad', 'Pune', 'Vadodara' are grouped together. With Indian restaurant being the 1st most famous type restaurant among them.\
4.The cities 'Bangalore', 'Faridabad', 'Hyderabad', 'Indore', 'Jaipur', 'Kanpur', 'Kolkata', 'Thane', 'Visakhapatnam' are grouped together. With South Indian restaurant being the 1st most famous type restaurant along with Indian Restaurant among them.\
5.The cities 'Mumbai', 'Patna', 'Surat',are grouped together. With Indian restaurant being the 1st most famous type of restaurant among them.\
6.The cities 'Chennai', 'Lucknow', 'Ludhiana',are grouped together. With Indian restaurant being the 1st most famous type of restaurant among them.

## Discussion
There is a small discrepancy in the datasets. There are some entries in the dataset that just say 'Restaurant'. We can consider this type as a restaurant which serves different cuisines. We may be right or we may be wrong.

For some reason GitHub is not displaying Folium Maps, so these maps are included in a new folder called Map Images which can be found [here](https://github.com/Gautham000/Coursera_Capstone/tree/master/Final%20capstone/Folium%20maps)

## Conclusion
Hence, this notebook serves as a reference to identify the relations between food cuisines between the cities of India. This notebook can be extended to include not only the data related to restaurants but also other aspects like sports locations, entertainment venues, etc.
