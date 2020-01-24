# Geolocation-Tagging
Identify city , location and country based on Geo location data

Objective of the Scripts :--
---------------------------
Identify city ,province and country based on the lat,long values using the reverse geocoder api.
Update the user pandas dataframe with these values.
Create lookup table based on dictionary group by country where user visited along with the province and city pair in each country.

Complexity and perfomance
--------------------------
fetch_province_city_country --> Fetches values from the API for each captured locations. Best case is when the number of lat,long is less and worst case is when the number of data points is huge . O(n)

prov_city_count --> Traversing ordered dictionary , individual repsonses from the reverse geocoder identifying the province,city and country. each result would return one values corresponding to a lat, long location.  Worst and Best case O(1)

lookup_dictionary --> Grouping up by country and displaying province and city in a datafreme . Worst and best case in O(1)

Total complexity ---O(n)

person1.csv, person2.csv and person3.csv are the 3 sample input files used for the analysis.

datarefresh_design:
-------------------
A sample data refresh design flow diagram using the Foursquare API. A system that can receive a location fix (as a [latitude, longitude, accuracy] mobile GPS fix) and run an algorithm to find the actual venue a user has visited using Foursquare as a venues-database.The objective was to minimize the calls to the Foursquare API and include a way to refresh Foursquare results as data retrieved from Foursquare can only be kept for a maximum of 30 days.Keeping in mind the definition of accuracy for a mobile GPS fix.
