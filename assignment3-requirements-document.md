Due: Feb. 19
# Requirements Doc
### Weather Visualizations
#### Josh Alexander, John Connolly, Chris Kasza

## Preface
*This defines the expected readership of the document and describe its version history, including a rationale for the creation of a new version and a summary of the changes made in each version.*

## Introduction
*This describes the need for the system. It should briefly describe the system’s functions and explain how it will work with other systems. It should also describe how the system fits into the overall business or strategic objectives of the organization commissioning the software.*

Our system will serve up weather visualizations to clients via a user-friendly website. Our system interfaces with the OpenWeatherMap API to serve up the visualizations, and the system itself is a combination of front-end and back-end sub-systems. Our system attempts to achieve our overall goal of providing interesting and helpful weather graphs for a variety of clients. 

## Glossary
*This defines the technical terms used in the document. You should not make assumptions about the experience or expertise of the reader.*

**Data visualization:** A way of displaying data in a comprehensible manner for human consumption.

**API:** Application programming interface, an interface containing clearly defined methods for communication between programs, websites, data sets, etc.

**OpenWeatherMap:** An online service that provides free weather data via an API.

## User requirements definition
*Here, you describe the services provided for the user. The nonfunctional system requirements should also be described in this section. This description may use natural language, diagrams, or other notations that are understandable to customers. Product and process standards that must be followed should be specified.*

## System architecture
The system architecture will follow modern techniques for building webpages. Specifically the frontend and backend will be divided into their own services.  The frontend is written in HTML/CSS/JavaScript. The CSS framework, Bulma, is being leveraged along with the Nuxt.js, a JavaScript framework built on top of Vue.js. The backend will be written in python and use the django framework.  The staging site for the backend is Heroku.com and for the frontend it is Netlify.com. The production server will be a custom build on a DigitalOcean.com VPS.

## System requirements specification

### Functional Requirements:
The application must provide varied weather graphs.  
The application must be hosted on and accessible via the web. 
The application must be viewable on a variety of devices (mobile, tablet, desktop, TV, etc).

### Non-functional requirements:
Three months of part time developer time is not sufficient to produce a fully functioning weather application to compete in the existing market space.
Hypothetically, if the application was fully implemented and could compete in the market, the resources used to host it are not configured to scale to meet demand. And the group is not in a position to pay for the underlying compute power to support a scaling solution.

## System models
*This chapter includes graphical system models showing the relationships between the system components and the system and its environment. Examples of possible models are object models, data-flow models, or semantic data models.*

## System evolution
*This describes the fundamental assumptions on which the system is based, and any anticipated changes due to hardware evolution, changing user needs, and so on. This section is useful for system designers as it may help them avoid design decisions that would constrain likely future changes to the system.*

The system is not expected to have hundreds of clients per day, but should be ready to expand easily in the event of increased demand. 

The free version of OpenWeatherMap allows for 60 responses per minute, we would have to purchase a plan for more requests if they become neccessary due to high demand. We can not afford this, so this is a limiting factor for our system.

The database contains just data from the OpenWeatherMap, and we are right now not planning on storing anything else. The rate of expansion required for the database should be constant, and there are no foreseen rapid expansions planned.

The system will only provide Canadian weather data to start. It is out of the scope of this project to provide international weather data. However, this could be an evolution that may come up later.

## Appendices
*These provide detailed, specific information that is related to the application being developed—for example, hardware and database descriptions. Hardware requirements define the minimal and optimal configurations for the system. Database requirements define the logical organization of the data used by the system and the relationships between data.*

## Index
*Several indexes to the document may be included. As well as a normal alphabetic index, there may be an index of diagrams, an index of functions, and so on.*
### Figures Index
Figure 1: View Visualization Sequence Diagram
Figure 2: Use-case Diagram

# Include "X" of the following:
## User interface description 
## System interface description 
## References 
## Some of the diagram types
*Context, Process, Use-case, Sequence, Activity, State*
