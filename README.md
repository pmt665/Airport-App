# Airport-App

Airport App
Assignment Components Deliverable:
1) API 
2) User Interface 
API gateway provides following API as mentioned below:
•	api/airports
This API returns all the airports for Europe continent by calling external API. This api is called after every 5 minutes and if it gets data successfully from externalApi a custom header ‘from-feed’ is added with value “success” stating response received successfully otherwise “ failure” is added to ‘from-feed’ header.
               
•	api/airports/countries
This API returns all the country names and iso codes for Europe continent by calling external API. This api is used to display all the countries in the UI so that user can filter the airports based on the country.
Note: Following external Api is used to get the countries for the Europe.
    https://restcountries.eu/rest/v2/regionalbloc/eu                         

•	api/airports/{isoCode}
This API returns all the airports as per the country selected in the UI. This api accepts one required parameter as “isoCode” which is used to filter out the airports based on the country.                      

•	api/airports/CalculateDistance
This API returns the distance between the two airports as per the user selection on the UI. This is the extra requirement mentioned in the assignment. It accepts “IataCodes” of two selected airports as QueryString in form of “IataCode1_IataCode2” so they are passed in the url and then Microsoft “GeoCoordinates” class is used to calculate the distance between the airports and returned the same to the user.                      

 
Following two classes are created to map the response returned from the External API:
 

User Interface:
Requirement 1:  Display all the airports for the Europe.
On start of the application below UI will be available for the user which shows all the airports and dropdown for the selection of country and a button to calculate the distance between the airports.
 

 
Requirement 2: Filter the airports based on the country selection.
Select the country: On selection of country only the airports for that country will be displayed in the grid.
 
Requirement 3:  Calculate the distance between two airports:
Calculate Distance: on Click of button user can select the airports and distance is calculated between them.
 
Technologies Used to develop the project: Angular 4, .NetCore, VS2017, MVC  
