# The_Battle_of_the_Neighborhoods
Utilizing the Foursquare API to analyze trends in the Toronto area. With the insight gained from this we will be able to advise for or against an investor setting up shop in this location.

Capstone Project - The Battle of Neighborhoods

The problem:
An investor seeks to open up a new business in the Toronto area. They are unsure of the kind of business that would flourish in the area due to not being accustomed to the ever changing trends of today’s times.
They would like an analysis done on the area that shows the top venues visited by locals and tourists.
With this data they can confidently invest the inheritance they received from their long lost grandmother.  

The data plan:
We will start our expedition by scraping data from the following Wikipedia page: (https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M)
This will be achieved using the pandas read_html function.
Once the extraction is complete we will create a dataframe of the data and clean it by removing any null values. 
We now need the geolocation data of all the concerned neighbourhoods. This will be obtained by using the Geocoder Python package. Once the geolocation data is pulled we create a new dataframe consisting of it. 
We now need to merge our two dataframes based on the matching “Postcode” column which is present in both dataframes. This can be achieved using the Pandas merge function.
With our newly combined dataframe we can plot a sample map to show the various neighbourhoods in Toronto using the Folium package. This will give us a good view and indication of the data.
Our data is now ready to be plugged into the Foursquare API.
We obtain the top nearby venues in each neighbourhood based on their Longitude and Latitude values.
With this we can create a new dataframe of each neighbourhood with the top ten most common or top venues.
With our newly formed dataframe consisting of the top venues of each neighbourhood, we are able to perform Kmeans clustering. 
The clusters can now be analyzed to make an informed decision regarding the new business.
