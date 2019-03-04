# Architecture Document

Description of Architectural Pattern/Style and why it was chosen
- backend system - MVT (model-view-template) pattern (synonymous with MVC [model-view-controller])
- frontend system - MVVM (model-view-viewmodel) pattern
- data storage system - RDBMS (relational database management system)

Django was chosen for the backend because of its popularity and its ease of use.  The Django backend makes use of MVC which is one of the most common design patterns.  MVC helps separate our logic and data into separate components making it easier to test.  A major design decision was deciding how create our front end.  We ended choosing to use Vue.js. Vue allows us to separate our backend and frontend into separate services, this allows us to have loosely coupled components that communicate with each other via a restful api.  Having separate services for front end and backend allow us to work on the different components concurrently.   The front end uses  MVVM (model-view-viewmodel) pattern.  The MVVM pattern helps separate logic even more.  This means that each model has less responsibly making things easier to test.   For our data storage system we chose to use a RDBMS (relational database management system) specifically postgresql.  This makes accessing our data easy and has strong guarantees over data consistency. 

Choice of technologies and why
- backend system - Django REST (representational state transfer) API (application programming interface)
- frontend system - Vue.js
- data storage system - PostgreSQL RDBMS

Abstract diagram of the architecture (like the packing robot example)

Answers to these questions

1. How will the structural components be broken into sub-components?
2. How will the system be distributed?
3. Which of these system characteristics will be prioritized, how, and why: performance, security, safety, availability, maintainability
