# SG_Relocation_recommendation
## Introduction

For many people, the idea of relocating to a new country is an exciting and daunting prospect. This could be for work commitments, or simply for a lifestyle change. Finding the right accommodation and housing is never easy. In this project I consider the city like Singapore because it is very attractive for expats around the world. When a foreigner is in Singapore, he or she might face difficulty finding an apartment, very much of a time is when you can't decide on the location, and you don't know what's best for your family and yourself. Consider the amenities nearby, like do I require an MRT nearby? Or do you need a supermarket nearby. These are also critical to your everyday life, as they will pose convenience.

So, in this project I am going to segment the Singapore into different neighborhoods using the geographical coordinates of different buildings, and the geographical coordinates of top 100  venues around this particular building (within 500 meters). Finally, I applied the machine learning to group the neighbourhoods into clusters.

## Business Problem

My project may be useful for real estate agencies (or relocation agencies) and their customers to find the right accommodation and house for them. For instance, Mr Smith currently staying at The Paterson Edge Condo. This condo is locate in the posh are Orchard whith a great neighborhood venues (MRT station, shopping centers, cinema, grocery stores, hospital, primary school). Howevere, Mr Smith's youngest daughter is going to an international school soon, which is located near East Coast Area. Therefore, Mr Smith would like to move to the new area, but with similar neighborhood. 
The neighborhood clustering approach is one of the possible recommendation system which Mr Smith may use in his search.

## DATA

The main dataset is collected from the open repository: https://github.com/xkjyeah/singapore-postal-codes. It provides the .json file which is a dump of all Singapore postal codes retrieved from Onemap.sg API. From the input json file I extracted only: 'Postcode', 'Building', 'Latitude', 'Longitude'. After cleaning data by removing all NIL values I got 155 744 rows. This is a big number. For a further analysis (and because I have a limit of using external libray like Foursquare API), I randomly select 500 buildings. Next, I found that some buildings, out of 500, appers multiple times. Therefore, after removing all duplicates I left with 353 unique Buildings.

In addition, to the building's geographical coordinates, I incorporated the Foursquare API, to extend my dataset. The final dataset contains  the building's names and their geographical coordinates, all venues names  within 500 meters and their geographical coordinates, and in addition venue's categories. In total I have 7371 rows, with 353 buildings, 3815 unique venues from 320 unique venue categories. All data are attached in this repository.
