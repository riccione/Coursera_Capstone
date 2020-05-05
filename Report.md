# Report

# Coursera Capstone - Business opportunities in Orlando, FL, USA

## April, 2020

## Introduction
Orlando is one of the most visited cities in the world primarily driven by tourism, major events, and convention traffic, in 2018 the city drew more than 75 million visitors. The two largest and most internationally renowned tourist attractions in the Orlando area include the Walt Disney World Resort, opened by the Walt Disney Company in 1971, and located approximately 21 miles (34 km) southwest of Downtown Orlando in Bay Lake; and the Universal Orlando Resort, opened in 1990 as a major expansion of Universal Studios Florida. With the exception of Walt Disney World, most major attractions are located along International Drive with one of these attractions being the Wheel at ICON Park Orlando. The city is also one of the busiest American cities for conferences and conventions; the Orange County Convention Center is the second-largest convention facility in the United States [Wikipepia](https://en.wikipedia.org/wiki/Orlando,_Florida). 

## Business Problem
I am going to do a project against Orlando, FL. Orlando, FL is an extremely popular touristic destination. The main attraction for tourist are theme parks. 
For this project I want to look at the different districts of Orlando and classify them. To split Orlando to districts I am going to use the simple approach – zip codes. Orlando contains 62 postal codes.
This will give an idea what kind of business work better in each district. It will be useful data for business, because it will help to choose the right district to run particular business.

## Data
I need the list of zip codes for Orlando, FL with geo coordinates (latitude and longitude)
1.	The best way to get it – download ready to use csv file from [ODS](https://public.opendatasoft.com/explore/dataset/us-zip-code-latitude-and-longitude/table/) using wget or curl directly in the Jupyter Notebook
2.	Foursquare API to explore venue types surrounding each zip. Foursquare outlines these high-level venue categories with more sub-categories. I’ll be querying the number of venues in a 1000m radius.
3.	I need to remove unused columns and data is ready to use.
4.	Analyze data with Pandas, visualize it with matplotlib and Folium, and then using k-mean clustering to cluster districts of the city.