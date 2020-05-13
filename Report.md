# Report

# Coursera Capstone Notebook: Clustering of Rome Subway stations

## May, 2020

## Rome, Italy

## Introduction
The Rome Metro (Metropolitana di Roma) started operation in 1955. It has three lines: A (orange), B (blue) and C (green). It has 73 stations, the length of it is about 60 km. The lines A and B intersect at Termini Station, which is also the main train station in Rome. Annually it serves for 279 million of people (2012).
We want to look at the areas surrounding metro stations and cluster them. The areas in the historical center of Rome have a lot of touristic attractions (Vatican, Colosseum, Trevi Fountain, Spanish Steps) and hotels. Some neighborhoods are in residential areas, other in commercial. The venues near to the station determine how people use it.
Analysis of data can show the primary purpose of the station. This data is useful for commercial business (location to open a new business), for local government (can help them in city planning), and for subway development in the future (where open new stations).

## Data
We need several pieces of data to start our study.
1. List of all subway stations and their geo data (latitude, longitude). The list of station is easy to get from [Wikipedia](https://it.wikipedia.org/wiki/Stazioni_della_metropolitana_di_Roma). However, this table does not contain geo data. To get geo data we can use prepared csv file [github]( https://raw.githubusercontent.com/riccione/Coursera_Capstone/master/Rome_Metro.csv), which contains list of the stations and geo data. By merging two sources of data we can get this dataset.
2. Foursquare API to explore venue types surrounding each station. Foursquare outlines these high-level venue categories with more sub-categories. 
* Arts & Entertainment (4d4b7104d754a06370d81259)
* College & University (4d4b7105d754a06372d81259)
* Event (4d4b7105d754a06373d81259)
* Food (4d4b7105d754a06374d81259)
* Nightlife Spot (4d4b7105d754a06376d81259)
* Outdoors & Recreation (4d4b7105d754a06377d81259)
* Professional & Other Places (4d4b7105d754a06375d81259)
* Residence (4e67e38e036454776db1fb3a)
* Shop & Service (4d4b7105d754a06378d81259)
* Travel & Transport (4d4b7105d754a06379d81259)
We will query the number of venues in each category in a 1000m (walking distance) radius around each station. This is the main way to analyse data, because I would like to have comparable data with similar project related to the Moscow subway [Classification of Moscow Metro stations using Foursquare data]( https://towardsdatascience.com/classification-of-moscow-metro-stations-using-foursquare-data-fb8aad3e0e4). Thank you for creation study against Moscow metro, it inspired me and move forward.