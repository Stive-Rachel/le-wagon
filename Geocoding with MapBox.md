Mapbox is a service used by large companies to obtain geographical information (maps, localisation, points of interests…).

We will use their API to find coordinates.


### 1- Go to 🔗 https://www.mapbox.com/ and find the API documentation.
+ https://docs.mapbox.com/playground/

### 2- From there, find the geocoding API documentation.
+ https://docs.mapbox.com/playground/geocoding/

### 3- What are the use cases for geocoding?
+ The Mapbox Geocoding API allows you to search for addresses and places by name (forward search) or coordinates (reverse search).

### 4- Create a Mapbox account and get your access token.
Use a signup button and fill in the form.
Verify your email address by following the instructions.

🚧 If you can, don’t use a gmail address as it will ask for your credit card info otherwise. After you finish, you will be given an access token to make API queries.

If you nonetheless continue to experience issues, you can use 🔗 https://developers.google.com/maps as an alternative.
+ Done!

### 5- Go back to the geocoding API documentation and find the forward geocoding example “Los Angeles”. What are the verb, scheme, host, path and query parameters?
** https://docs.mapbox.com/playground/geocoding/?search_text=Los Angeles **

+ verb :
+ scheme : https
+ host : docs.mapbox.com
+ path : /playground/geocoding/
+ query : search_text=Los Angeles

Hint

### 6- Find out how to use Insomnia to get the coordinates of the city centre of "Paris".
"coordinates": [
					2.3483915,
					48.8534951
				]

### 7- Find out how to use Insomnia to perform a reverse geocoding of your birthplace.
+ https://api.mapbox.com/geocoding/v5/mapbox.places/-61.53262407518599,16.239653341953243.json
