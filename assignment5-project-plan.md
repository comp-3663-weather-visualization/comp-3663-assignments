# Planning Document
## Weather Visualizations
#### Joshua Alexander, John Connolly, Chris Kasza

## 1. Introduction
#### Briefly describe project objectives and constraints
The objectives of our team is to make a user-friendly graph-centric website dedicated to representing the weather forecast in comparison with historical weather patterns. The final product must be easy to use, and most importantly, beautiful.

The main constraint is time, especially in combination with man-power. With three team-members in our project, and 3 months to make a fully-fledged project; the team's time is very constrained.

## 2. Project organization
#### People and their roles
Because of our small team, team members must take on multiple roles.

**Joshua Alexander:** Librarian, Documentation Editor, Support Programmer.

**John Connolly:** Chief Programmer, tester.

**Chris Kasza:** Backup programmer, language/system expert, project administrator.

## 3. Risk analysis
#### Possible risks, likelihood of those risks and risk reduction strategies

* Our website is dependent on OpenWeatherMap API to get our forecasts—if they were to disappear, even temporarily, our website be rendered inoperable. We need to rely on this API, and I see no way for this risk to be mitigated. If OpenWeatherMap were to go away, we would have to refactor our project to use a new API.

* We have a specific due date for this project (April 2nd). As with all projects with a due date, there is always a risk of not completing the project on time. A way of mitigating this risk is by making this document—it provides the team with a plan to guide us from now until April 2nd to get everything done on time.

* It is not free to host our website on a Droplet. If we wanted this project to live past April 2nd (the due-date), we would have to acquire funding from somewhere to keep our website up. There is always a risk in projects when it comes to funding, and ours is no exception. However, it is not likely that we will be required to host the website for more than a couple of weeks.

## 4. Hardware and software resource requirements
#### What will be used in the project

The front-end of our website uses a framework called Vue.js. Vue allows us to easily build the beautiful and reactive user interface needed in our project.

The back-end of our website uses a framework called Django. Django works very well with Vue, and our DBMS. Additionally, Django is fast, scalable, and maintainable—all good things for our project.

The database management system we will use is PostgreSQL. We picked this because all team members are familiar with PostgreSQL, and it interacts well with Django and Vue.

The server we are hosting our website on is a DigitialOcean virtual server (called a Droplet). A droplet scales incredibly easily as a virtual server—this ensures we will never have to change or manage hardware.


## 5. Work breakdown
#### Break into activities with inputs and outputs

###### T1: Project Brainstorming
* Input: Creativity.

* Output: An idea for a project that utilizes an open data source.

###### T2: Problem Statement
* Input: A creative idea.

* Output: A formalized project layout aiming to solve a problem and satisfy requirements.

###### T3: Requirements Document
* Input: Problem Statement.

* Output: A concrete list of requirements that we must satisfy with our project.

###### T4: Architecture Document
* Input: Requirements Document.

* Output: A hand-picked list of hardware and sofware, and their interactions to satisfy the needs of our project.

###### T5: API & Database Integration
* Input: Architecture Document, Requirements document, programmer time.

* Output: A working database that correctly pulls and stores data from the OpenWeatherMap API to satisfy our requirements.


###### T6: Back-end Prototype
* Input: Architecture Document, programmer time.

* Output: A working prototype back-end.


###### T7: Front-end Prototype
* Input: Architecture Document, programmer time.

* Output: A working prototype front-end.


###### T8: Front-end & Back-end Integration
* Input: A working back-end and front-end, programmer time, architecture document.

* Output: A working website that is able to be hosted to the internet.

###### T9: Test writing
* Input: An intermediate working system.

* Output: A test suite that should run on the final project.

###### T10: Completed Graphs
* Input: A completed database and functional front-end.

* Output: Two graphs that fulfil our user-requirements and are ready to be added to the front-end.


###### T11: UI Design
* Input: Lots of creativity.

* Output: A beautiful UI to showcase what our future website will look like.


###### T12: Final Front-end UI Implementation
* Input: A beautiful UI design, a prototype front-end.

* Ouput: A beautiful front-end that looks as close as possible to our UI design.

###### T13: Hosting Website
* Input: A working website that can be hosted.

* Output: A hosted website that can be accessed through the internet.

###### T14: Finishing Touches
* Input: The feature-complete project.

* Output: The final version of the project.


###### T15: Project Presentation
* Input: The final version of the project.

* Output: A presentation that can be delivered to the class.


## 6. Project schedule
#### Show dependencies, estimated time and people allocation

## 7. Monitoring and reporting mechanisms
#### Management reports and project monitoring

The project is hosted on Github.com which has a full commit history so everyone can see what work was done. This provides a transparent window into how much work is done and how often.

Additionally, our team has a weekly project-status meeting on Thursdays where we all decide what must be done for the week, and doll out the jobs based on the capabilities of our team members.

At this meeting, we convene on the previous week's jobs and how they went and what we could do better in the next week. Because our team is so small, we do not need any external software to track our task's completion and progress—we are a small enough team to keep track of the week's tasks via person-to-person communication.

Now that we have officially divvied up tasks in this document, we can compare our progress to the project schedule above (and graphs below) to more precisely see how on-track we are in the project.

## 8. Diagrams:
#### Tasks, durations, and dependencies
![tasks](/Pics/tasks_graph.png)

#### Activity Chart
![activity](/Pics/activity_chart.png)
#### Staff Allocation Chart
