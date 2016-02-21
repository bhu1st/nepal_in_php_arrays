/******
 * @Some Rights with Bhupal Sapkota
 * @link http://github.com/bhu1st/nepal_in_php_arrays
 * @author Bhupal Sapkota (sapkotabhupal@gmail.com)
 * @url http://bhu1st.blogspot.com
 * @remark please link back to my blog if you use it.
 ****/
 
What is Nepal in PHP Arrays - Project ?
------------------------------------------

Are you a PHP developer? or say you use MySQL in your projects. How many of have easier access to the places & cities of Nepal in simpler arrays, that can be taken for reference and used. I am currently involved in a project named Gharbeti.com (http://www.gharbeti.com) and got in situation where i need to use the places in Kathmandu to implement the site theme - Gharbeti.com - Rentals In Kathmandu. 
 
I was searching through web, searching for some arrays of places, cities, districts headquarters etc. But i was not lucky enough to find them. Instead i thought i would search for places and list them as PHP Arrays or MySQL tables. This http://en.wikipedia.org/wiki/Districts_of_Nepal wiki page was handy though. 
 
There is a project named PHP Arrays - http://github.com/debuggable/php_arrays I was solely inspired by this project. But, limiting myself to my country i decided to list resources related to Nepal in PHP arrays. This is how all it begun. 
 

What is included in this project
--------------------------------

 1. Places In Kathmandu - PHP Array & MySQL table
 -> listing of most popular places in Kathmandu. 
	-places_in_kathmandu.php
	-places_in_kathmandu.sql	
 
 2. 14 Zones & 75 districts of Nepal 
 -> 14 Zones (Anchals), 75 (Districts/Headquarters)
	-14_zones_75_districts_of_nepal.php
 
 3. 75 Districts of Nepal and their Latitude & Longitude values. 
	-> 75_districts_latitude_longitude.php
	
	-> If you want to calculate Latitude Longitude values by yourself: here's a little snippet using Google Maps API that we can loop through by yourself.
	
		$country = "Nepal";
		$city = "Kathmandu";
		$addEncoded = urlencode($country).",+".urlencode($city);
		$geoCode = file_get_contents("http://maps.google.com/maps/api/geocode/json?address=".$addEncoded."&sensor=false");                    
		$response = json_decode($geoCode);
		$lat = $response->results[0]->geometry->location->lat;
		$lng = $response->results[0]->geometry->location->lng;
	-> Pick up any latitude, longitude pair and try browing in the following link format: 
		This link should bring out Map for Chitwan district: http://maps.google.com/maps?q=27.529131,84.3542049

Do you want to contribute to this Project? 
------------------------------------------
Use the github repo url, clone a local copy of the project, make changes, add files and push to the repo. don't forget to add to the changelog.


List of files:
---------------
1. 14_zones_75_districts_of_nepal.php - 14 Zones & 75 Discticts with Headquarters. 
2. 75_districts_latitude_longitude.php - Latitude/Longitude Array for 75 districts of Nepal
3. places_in_kathmandu.php - PHP Array for places in Kathmandu
4. places_in_kathmandu.sql - MySQL table for places in Kathmandu
5. readme.txt - this file 


