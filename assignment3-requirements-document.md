# Requirements Doc
### Weather Visualizations
#### Josh Alexander, John Connolly, Chris Kasza

## 1. Preface
### 1.1 Revision History
| Version | Date       | Comment                               |
| -------:|:----------:| ------------------------------------- |
| 1.1     | 2019-03-05 | Add context in sections where lacking |
| 1.0     | 2019-02-26 | Initial description                   |

### 1.2 Audience
This document is written for the developers of this software project as a reference point of what should be developed and delivered and to avoid feature creep. Considering this software project is being developed as a requirement of the class, COMP 3663 X2, at Acadia University, it is expected that the professor, and possible teaching assistants, will read the document as well.

## 2. Introduction
Our system will serve up weather visualizations to clients via a user-friendly website. Our system interfaces with the OpenWeatherMap API to serve up the visualizations, and the system itself is a combination of front-end and back-end sub-systems. Our system attempts to achieve our overall goal of providing interesting and helpful weather graphs for a variety of clients.

Our system will be more focused on easy to generate historical visualizations than weather forecasts. There are many easy to find websites that provide weather forecast data and visualizations. In comparison, generating charts representing historical weather data in a aesthetic and customizable way is harder to find. 

## 3. Glossary
**API:** Application programming interface, an interface containing clearly defined methods for communication between programs, websites, data sets, etc.

**Backend:** Refers to the portion of the web application that runs on a server. Think of the user's browser as the client and the backend is the server the client connects to. The backend handles the interaction with the database, any heavy computations, and delivering data to the frontend.

**Django:** An MVT (model-view-template) framework written in Python. Provides both a backend and a frontend but the system being built will only use Django to deliver an API. [1]

**Framework:** A framework is a generic abstraction/platform that provides functionality that is usually focused on *ease of programming* or the ability to make beautiful things easily (when dealing with web frameworks). 

**Frontend:** Refers to the portion of a web application that a user directly interfaces with. The portion that renders on in the user's web browser.

**HTML/CSS/JavaScript:** These are all programming languages that makeup websites. HTML (hypertext markup language) is the content, CSS (cascading stylesheets) is the styling, and JavaScript is extra functionality, like animations, events, etc.

**Nuxt.js:** A JavaScript framework that extends the functionality of the Vue.js framework. It allows for rapid development and delivery of a modern JavaScript frontend. [2]

**OpenWeatherMap:** An online service that provides weather data via an API. There are free and paid tiers to their service. [3]

**VPS:** Virtual Private Server. A virtual machine provided as a rentable service via a web host such as DigitalOcean or Linode.

## 4. User requirements definition
4.1. The system shall be accessible as a web application from anywhere in the Canada provided the user has a computer with an Internet connection and a modern web browser (Firefox, Chrome, Safari, Opera, Microsoft Edge, etc.).

4.2. The system shall not require authentication or user accounts. Users access the services provided by the web application on demand with ease.

4.3. The system shall determine the user's current geographic location if location services are permitted via the web browser. 

4.4. Upon initially browsing to the web application, the user will receive the current weather information for their geographic location if the location service is enabled; otherwise, the system will default to Toronto, ON, the center of the country.

4.5. The system shall provide the user the ability to change the location from the default to any other community in Canada. Changing the community will automatically display the current weather for the selected community.

4.6. The system shall provide the ability two display two temperature charts.

4.6.1. The first temperature chart will display line graph with temperature displayed in the Y-axis and time in the X-axis. The user will select the start and end time for the time frame.

4.6.2. The second chart will also display a line graph of temperature. The difference is that the user chooses two time frames to compare. The user will select the start time for each time frame and then specify a duration that will be used for both.

4.6.3 The time frame for the graphs shall be able to be changed via a drop down between various different times (eg. 1 year).

4.7. There shall be a input element to change the unit of the temperature between Celsius, Farenheit and Kelvin.

4.8. There shall be an input element to search for different locations to view their local weather.

## 5. System architecture
The system architecture will follow modern techniques for building web sites. Specifically the frontend and backend will be divided into their own services.  The frontend is written in HTML/CSS/JavaScript. The CSS framework, Bulma, is being leveraged along with the Nuxt.js, a JavaScript framework built on top of Vue.js. The backend will be written in Python and use the Django framework.  The system gathers information from OpenWeatherMaps API rather building a weather station and collecting our own data.  The staging site for the backend is Heroku.com and for the frontend it is Netlify.com. The production server will be a custom build on a DigitalOcean VPS. The database to hold the data gathered from the API is PostgreSQL

## 6. System requirements specification

### 6.1. Functional Requirements:
6.1.1. The system must provide temperature graphs.  

6.1.2. The system must be accessible via the web. 

6.1.3. The system must be viewable on a variety of devices (mobile, tablet, desktop, TV, etc).

6.1.4. The system must be highly available and not experience downtimes.

6.1.5. The system must access the OpenWeatherMap API and fetch new data every sixty minutes.

6.1.6. The system must allow selection of different locations.

6.1.7. The system must allow for displaying different time ranges in the graphs.

6.1.8. The system must allow switching between different temperature units.


### 6.2. Non-functional requirements:
6.2.1. The system should be outfitted with an aesthetically appealing colour pallete.

6.2.2. The system should maintain a consistent aesthetic while being responsive (viewable on a variety of different screen sizes).

6.2.3. The system should be fully accessible in future releases.

6.2.4. The system should transition between different location selections gracefully.

6.2.5. The system should fetch and load the appropriate data within 300 milliseconds.

6.2.6. The system should have aesthetic input elements and graphs that please the eye with a certain je ne sais quoi.


## 7. System models

![diagram1](Pics/SequenceDiagram.jpg)

![diagram2](Pics/UseDiagram.jpg)

## 8. System evolution

The system is not expected to have hundreds of clients per day, but should be ready to expand easily in the event of increased demand. 

The free version of OpenWeatherMap allows for 60 responses per minute, we would have to purchase a plan for more requests if they become neccessary due to high demand. We can not afford this, so this is a limiting factor for our system.

The database contains just data from the OpenWeatherMap, and we are right now not planning on storing anything else. The rate of expansion required for the database should be constant, and there are no foreseen rapid expansions planned.

The system will only provide Canadian weather data to start. It is out of the scope of this project to provide international weather data. However, this could be an evolution that may come up later.

## 9. User interface description

The goal of the user interface is to be simple and intuitive. As stated in the user requirements, a user browses to the web application and is presented with the current weather information for their geographic location (or Toronto if location services is disabled). 

Clicking the community name will expose an input field with an automatically filtered drop down. The user can enter in a different community name in the input field and the system will automatically display a list of options that the user can select. The current weather data will automatically change to reflect the newly selected community.

In top center of the page, there shall be two tabs, Home and Graphing. Clicking Home will return the user to the home page which displays the current weather information and click Graph will display the graphing page.

The initial display of the graphing page will display a chart with last year's temperature data for whichever community the user previously chose.

Above the chart will be a toggle to switch between the single line chart and the comparison chart. To the right of the toggle will be the drop down to select the time frames used in the chart.

## 10. System interface description 

Key components in the system are the database, Django backend, and Nuxt.js frontend.

Every sixty minutes, a job will kick off in Django that queries the OpenWeatherMaps API for the current temperature of all of the communities and saves those temperatures to the database. Django provides an interface to common databases out of the box.

The Django backend will provide three RESTful API endpoints that the Nuxt.js frontend will query to retrieve data.
1. GET communities - returns a list of the communities available to be viewed
2. POST current - provided a community ID, the endpoint will return the current weather information for the given community
3. POST temp_range - provided a community ID and a date range, the endpoint will return an array of temperature values

## 11. References

[1] "Django Documentation | Django", Djangoproject.com, 2019. [Online]. Available: https://docs.djangoproject.com/en/2.1/. [Accessed: 05- Mar- 2019].

[2] "Introduction - Nuxt.js", Nuxtjs.org, 2019. [Online]. Available: https://nuxtjs.org/guide. [Accessed: 05- Mar- 2019].

[3] "Weather API - OpenWeatherMap", Openweathermap.org, 2019. [Online]. Available: https://openweathermap.org/api. [Accessed: 05- Mar- 2019].

## 12. Index
### Figures Index
Figure 1: View Visualization Sequence Diagram

Figure 2: Use-case Diagram
