# Problem Statement
### Weather Visualizations
#### Josh Alexander, John Connolly, Chris Kasza

## Brief Introduction
The world needs more weather visualizations. We'll provide historical and real-time visualizations of weather. We'll use Canadian data to start but the solution will be location agnostic.

## Define problem
We are looking to provide a detailed, visualization-focused analysis of historical and real-time weather. The world, specifically people who enjoy looking at graphs and data visualizations, could benefit from our amazing and varied weather visualizing techniques. From casual visualization-viewers, to full-time graph-enthusiasts -- anyone may benefit from our weather visualizations.

## Use scenario for each member of group
Each member of the group will be responsible for developing supporting documenation and reports as well as code. Depending on experience and interest, group members may be contribute more to the frontend code or backend.

## Functional and non-functional requirements
### Functional Requirements:
The application must provide varied weather graphs.  
The application must be hosted on and accessible via the web. 
The application must be viewable on a variety of devices (mobile, tablet, desktop, TV, etc).

### Non-functional requirements:
Three months of part time developer time is not sufficient to produce a fully functioning weather application to compete in the existing market space.
Hypothetically, if the application was fully implemented and could compete in the market, the resources used to host it are not configured to scale to meet demand. And the group is not in a position to pay for the underlying compute power to support a scaling solution.

## System limitations
The system will only provide Canadian weather data to start. It is out of the scope of this project to provide international weather data.

## Development Environment
The backend is written in Python using the Django framework and a PostgreSQL database.

The frontend is written in HTML/CSS/JavaScript. The CSS framework, Bulma, is being leveraged along with the Nuxt.js, a JavaScript framework built on top of Vue.js.

Revision control for both code bases is handled with git and backed up to GitHub.com. Development of features and bug-fixes is completed in separate repository branches, then merged to master after a code review. The code in master is automatically deployed to a staging site for review and user testing. When development is complete and the staging site has passed user testing, it will be pushed to the production site.

The staging site for the backend is Heroku.com and for the frontend it is Netlify.com.

The production server will be a custom build on a DigitalOcean.com VPS.

## Deliverables
- Feb 19: Requirements document
- Feb 26: Unit tests
- Mar 05: System specification document
- Mar 12: Architecture documents
- Mar 19: UI design documents
- Apr 04: Final deployment and code delivery
