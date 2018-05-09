# Quiz_App
The Quiz App generate a question and four optional answers when a user is in close-proximity to a point of interest (POI)

The Quiz App displays a question for the user once they are in close-proximity to a point of interest (POI). The location of the user is tracked and a multiple-choice question pops up when they are 5 metres from a given point. The question is specific to the POI. For example, a question about the age of UCL could be created if a user was near UCL. An answer is selected by the user and an alert is created by the system to notify the user if they are right or wrong. The answers and phone ID are uploaded to a database when the user submits their final answer. A new question pops up when the user moves to a new location.

There are 4 files in the Quiz Repository that are used to achieve functionality in the Quiz App. The ‘index.html’ file has code relating to the app design, the ‘upload.Data.js’ relates to transferring data into the database, ‘appActivity.js’ relates to functions used in the quiz activity, and ‘httpServer.js’ allows data transfer between database and App. The user guide is labelled 'Quiz_Guide.html' in the www directory. A link in the navigation bar and dropdown menu of the (index) HTML file has been created to retrieve information about using the Quiz App.

The Quiz App requests quiz data from the PostgreSQL database which is then inserted into the map or parsed to acquire individual data (e.g. question). The location of quiz points are identified by a blue marker and the user's location is identified by a red marker. Distance from the user's location to a quiz point is calculated using the haversine formula. If the user is within 5 metres from a POI, a quiz popup will be generated at the location on the map. The database generates a question relating to movie scenes that were shot in UCL and there are four alternative answers (‘Inception’, ‘Spiderman’, ‘Thor’ and ‘Transformers’) which are inserted as checkboxes. The user can select one of these answers and an alert message indicates whether they are right or wrong. The database contains the correct answer which is matched against the value of each checkbox. If they match, an alert message is created to notify the user that they are correct. If they don’t match, an alert message is created to notify the user that they are incorrect. The selected answer(s) and phone ID value is inserted into the database once the user presses the submit button.The user's position is tracked and the procedure can be repeated when the user is at a new location.

**References for the Quiz App**
[uploadData.js Code adapted from UCL CEGEG077 Module, Week 6 and 7:Creating a Data Server (API), accessed 18th April 2018, Also available from: https://github.com/claireellul/cegeg077-week6formcode/blob/master/ucfscde/www/js/uploadData.js ]

[index.html Code adapted from Material Design - : https://getmdl.io/templates/index.html, accessed 23rd April 2018]

[appActivity.js Adding a Leaflet Map: Code adapted from https://leafletjs.com/, accessed 25/04/2018 and UCL CEGEG077 Module, Week 1:Leaflet and Javascript Part 1, accessed 21st April 2018, Also available from: https://github.com/claireellul/cegeg077-week5app/blob/master/ucfscde/www/js/appActivity.js

Get LatLngBounds: Code adapted from https://leafletjs.com/reference-1.3.0.html#latlngbounds, accessed 26th April 2018,

AJAX HttpRequest: Code adapted from https://www.w3schools.com/xml/xml_http.asp, accessed 27th April 2018 and UCL CEGEG077 Module, Week 5:Creating an HTTPS Server, accessed 22nd April 2018, Also available from: https://github.com/claireellul/cegeg077-week5server/blob/master/httpServer.js

Haversine Distance Between Two Points: Code adapted from https://www.htmlgoodies.com/beyond/javascript/calculate-the-distance-between-two-points-in-your-web-apps.html, accessed 19th April 2018, Also available from: https://github.com/claireellul/cegeg077-week1/blob/master/getDistance.html

Track location of User: Code adapted from https://www.w3schools.com/html/html5_geolocation.asp, accessed 26th April 2018. Also available from: https://github.com/claireellul/cegeg077-week4/blob/master/ucfscde/www/js/appActivity.js]
