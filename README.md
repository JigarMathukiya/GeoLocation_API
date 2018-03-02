# GeoLocation_API

Create a repo on github or bitbucket, please name it "apitest"
 
use any language, but you have to use postgresql
Database setup : (NOTE: Enable geolocation features in Postgresql with extensions : cube and earthdistance.
Use the specific data types to create latitude and longitude
 
create a new table in postgres and load this CSV that denotes the mapping between pincode and lat/long (https://github.com/sanand0/pincode/blob/master/data/IN.csv).
Create Two APIs in flask : Get,Post.
Post : Post lat,lng of any location with pin code+address+city and you can add new pin code in db. This api will be /post_location. Remember to check if pin code
already exists or if there are existing latitude+longitude THAT ARE CLOSE ENOUGH TO BE THE SAME (dont assume that they will exactly be the same.)

Get : There are two GET apis. Given a location, fetch all the nearby pin codes within a radius. For example, I can ask - give me all points within 5km radius
of (45.12, 71.12) . To do this you will need to do mathematical computation of radius. there are two ways to do this:
You can use postgres "earthdistance" to compute all points in 5km radius. This api will be /get_using_self
Implement the mathematical computation yourself. this api will be /get_using_self
 
