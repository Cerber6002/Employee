# Airline Ticket Managment System

## Table of Contents
1. [Youtube](#youtube-video)
2. [Presentation](#presentation)
3. [Description](#description)
4. [Project Requirements List](#project-requirements-list)
5. [Team Members List](#team-members-list)
6. [Roles of Group Members](#roles-of-group-members)
7. [Screenshots](#screenshots)
8. [UML Class Diagram](#uml-class-diagram)
9. [Weekly Meeting Documentation](#weekly-meeting-documentation)
10. [Github Repository](#github-repository)
11. [Jar File Build](#jar-file-build)
   
    

## YouTube Video
Link on YOUTUBE - https://youtu.be/T9uMdnjUhpA 

## Presentation 
Link on presentation - https://www.canva.com/design/DAGZbz846IY/Qqwkz-mMVDkCkmYv_iFdRg/edit?utm_content=DAGZbz846IY&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

## Description
The Airline Ticket Management System allows users to book, manage, and cancel flights through an intuitive interface, and also supports administrative functions.

## Project Requirements List
The following key functionalities are essential for the completion of the project:
1. **User Registration**: Allow users to register by providing essential information such as name, email, and password.
2. **Login**: Enable registered users to log in securely with email and password credentials.
3. **Adding Tickets**: Provide the ability to add new tickets, including details such as flight ID, seat number, and ticket price.
4. **Ticket Search**: Implement a search feature to quickly find tickets based on parameters like ticket ID or flight ID.
5. **Ticket Booking**: Facilitate ticket booking by assigning tickets to specific customers, confirming availability, and processing the booking.
6. **Booking Cancellation**:  Allow users or administrators to cancel a booking and update the ticket status accordingly.
7. **Administrative Functions**: Enable administrators to perform tasks such as managing flights, viewing user details, and generating reports.
8. **Database Connection Using DAO**: Ensure secure and efficient data operations by utilizing the Data Access Object (DAO) pattern for all database interactions.
9. **Implementation of MVC Architecture**: Follow the Model-View-Controller design pattern to separate data, user interface, and control logic for better maintainability.
10. **Exception Handling for Invalid Input**: Automatically clear the input fields after adding or editing employee records.
11. **UML Class Diagram**: Present a well-structured UML class diagram showcasing the relationships and attributes of the system's classes.
12. **Creating a JAR File**: Add project to the database and project information like title, description, dates. Package the application into a JAR file for easy distribution and execution.

## Team Members List
- **Zhumadilov Uranbek** 
- **Zhyldyzbekov Sultan** 
- **Gairatbekov Kasymbek** 

## Roles of Group Members
- **Zhumadilov Uranbek**: - Project Manager, Database Administrator, Backend Developer
- **Zhyldyzbekov Sultan**: - Tester, UI/UX Designer, Content Creator
- **Gairatbekov Kasymbek**: - Database Administrator, Backend Developer, Frontend Developer

## Screenshots
Below are key screenshots showcasing the application:
- **Welcome**: ![Welcome]("C:\Users\User\Pictures\Screenshots\Welcome.png")
- **Registration**: ![Registration]() ![Registration](/assets/employees/Employee2.png) 
- **Login**: ![Login](/assets/edit/edit1.png) 
- **Seaarch**: ![Search](/assets/grades/Grades1.png) 
- **Flights**: ![Flights](/assets/trash/Trash1.png) 
- **Ticket**: ![Ticket](/assets/db/psql1.png) 
- **DataBase**:![Database](/assets/db/psql1.png) 

## UML Class Diagram
The UML class diagram provides a visual representation of the system’s structure, detailing the classes, attributes, methods, and their relationships.
![UML Diagram](UML/employeeperformanceapp3.png)

### Diagram Description:
- **Employee**: Represents employee details with attributes like `name`, `department`, and `hireDate`.
- **EmployeeGrade**: Extends `Employee` and adds an additional property `grade` to store the evaluation score.
- **EmployeeDAO**: Handles database operations for managing employees and grades.
- **EmployeeDAOInterface**: Interface for CRUD operations related to employee records.
- **HelloController**: JavaFX controller that handles UI interactions, including employee addition, modification, deletion, and evaluation.

## Weekly Meeting Documentation
Weekly meeting summaries and action items can be found in the [Google Docs link](https://docs.google.com/document/d/1E4ld5ssIVgZshUG-lhLDjgzNAuSk3Rkg3Ik92CVwCgI/edit?usp=sharing).


## GitHub Repository
The project source code and documentation can be accessed on GitHub at [GitHub Repository Link](https://github.com/EMMMABK/Employee-Performance-Evaluation-System.git).

## Jar File Build
