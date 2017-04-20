# I N E E D C O F F E E
## A web application to find coffee shops near you.
#### Author: Sean Krinik

## About:
**INC** short for **I Need Coffee** is a javascript web application that utilizes a few different tools like the Google Maps javascript API, Foursquare API and KnockoutJS framework.

The app uses your location so please enable location services. The top 25 coffee shops from a Foursquare search will be shown on the map. You'll see a button that says **hipsterify**. Clicking this will enter *"hipster mode"* and filter out any large chains from the results giving you a selection of only local or smaller chain coffee shops for you to try out. the **UN-hipsterify** button un-toggles hipster mode showing you large chains as well.

The search bar uses the Google Geolocation API to help you search for coffee in other places. Suppose you are heading on a road trip later today, just search your destination and find what shop you want to hit once you arrive! Make sure to use hipster mode so you choose something local.

## Functionality:

All calls to Foursquare & Google are asynchronous requests. I included the sources for solutions I found online for the obstacles I faced.

KnockoutJS is used to handle all DOM manipulations outside of the map. observable arrays store the markers for the map, but the markers themselves are NOT observable objects.

One notable improvement I was able to find online was the ability to create links to open the infowindows as listeners for each marker. You can click the name of a store in the list and see it's marker and infowindow on the map.

## Notable Challenges/Issues:

A few issues came with the Foursquare data. I wanted to display more info in the infowindows, but the information I got back from the ajax from Foursquare was limited and inconsistent. Additionally, when I ran a static call in the browser, I was able to get consistent results. Not sure if typing a call into the address bar differs from what you get when you call ```$.getJSON(...)``` but it seems to be a hurdle. Therefore, I only included the names of the shops for now.
