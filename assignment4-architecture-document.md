# Architecture Document

**Description of Architectural Pattern/Style and why it was chosen**
- backend system - MVT (model-view-template) pattern (synonymous with MVC [model-view-controller])
- frontend system - MVVM (model-view-viewmodel) pattern
- data storage system - RDBMS (relational database management system)

Django was chosen for the backend because of its popularity and its ease of use.  The Django backend makes use of MVC which is one of the most common design patterns.  MVC helps separate our logic and data into separate components making it easier to test.  A major design decision was deciding how create our front end.  We ended choosing to use Vue.js. Vue allows us to separate our backend and frontend into separate services; this allows us to have loosely coupled components that communicate with each other via a restful api.  Having separate services for front end and backend allow us to work on the different components concurrently.   The front end uses  MVVM (model-view-viewmodel) pattern.  The MVVM pattern helps separate logic even more.  This means that each model has less responsibility making things easier to test.   For our data storage system we chose to use a RDBMS (relational database management system) specifically PostgreSQL.  This makes accessing our data easy and has strong guarantees over data consistency. 

**Choice of technologies and why**
- backend system - Django REST (representational state transfer) API (application programming interface)
- frontend system - Vue.js
- data storage system - PostgreSQL RDBMS

**Abstract diagram**

![architecture](/Pics/Arch.png)


**How will the structural components be broken into sub-components?**

The structural components are broken into sub-components by decomposition.  For instance in our Vue.js front end we have a module for components that contains the subcomponents which make up our web page.  This allows for are components to be easily understood as they do only one thing. Similarly in our Django backend we decompose our route handler to have their own controller and corresponding model class for contain the views state. 

**How will the system be distributed?**

The application will be distributed via the internet; by building a web based application it allows us to distribute the application easily to a wide variety of devices without have to worry about specify hardware requirements.  

**Which of these system characteristics will be prioritized, how, and why: performance, security, safety, availability, maintainability**

When designing our application we chose to prioritize maintainability.  By using off the shelf components and having them loosely coupled, the program is easier to understand, repaired and extend.  In many software projects maintenance is often one of the largest costs; therefore, we have chosen to minimize them by prioritizing maintainability. 

Our application does not collect any user data, it only displays data to users.  The biggest threat to security will be a DOS (Denial of Service) attack; however, the value of the information being displayed doesn’t have significant value so the likelihood of a DOS attack would be quite low; therefore this is not our main priority. 

Lastly, performance, safety and availability are not prioritized because of they do not have a large impact on the our intended users or the project costs
