# Quiz_App
The quiz app to generate a question and four optional answers when a user is in close-proximity to a point of interest (POI)

The objective of the Quiz App is to generate a question for the user once they are in close-proximity to a point of interest (POI). The location of the user is tracked and a multiple-choice question pops up when they are within a specific distance from a given point. The question relates to the POI. For example, a question about the number of students at UCL could be created if a user was near UCL. The user selects an answer and the system notifies them if they are right or wrong. The answers and phone ID are uploaded to a database when the user submits their final answer. A new question pops up when the user moves to a new location. 

There are 4 files that are used to achieve functionality in the Quiz App.  The ‘index.html’ file has code relating to the app design, the ‘upload.Data.js’ relates to uploading data into the database, ‘appActivity.js’ relates to quiz functions, and ‘httpServer.js’ allows data transfer between database and app. 

Quiz data from the PostgreSQL database is requested and inserted into the Quiz App. A marker is inserted on a map to identify the location of the quiz points. The code incorporates the  haversine formula to calculate the distance between a user and a POI. The user has to be less than 5 metres from the POI to create a quiz popup on the map. For example, when a user is less than 5 metres from the front gates of UCL, a popup is created to ask the user what movie had scenes filmed in UCL. There are four alternative answers ‘Inception’, ‘Spiderman’, ‘Thor’ and ‘Transformers’ that are inserted as checkboxes. The user can select on of these answers and an alert message indicates whether they are right or wrong. The database contains the correct answer which is matched against the value of each checkbox. If they match, an alert message is created to notify the user that they are correct. If they don’t match, an alert message is created to notify the user that they are incorrect. The selected answer(s) and phone ID value  is inserted into the database once the user presses the submit button. 

