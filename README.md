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

## Presentation - https://www.canva.com/design/DAGZbz846IY/Qqwkz-mMVDkCkmYv_iFdRg/edit?utm_content=DAGZbz846IY&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

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
- **Employee**: ![Employee]() ![Employee](/assets/employees/Employee2.png) ![Employee](/assets/employees/Employee3.png) ![Employee](/assets/employees/Employee4.png)
- **Edit**: ![Edit](/assets/edit/edit1.png) ![Edit](/assets/edit/edit2.png) ![Edit](/assets/edit/edit3.png)
- **Grades**: ![Grades](/assets/grades/Grades1.png) ![Grades](/assets/grades/Grades2.png) ![Grades](/assets/grades/Grades3.png) ![Grades](/assets/grades/Grades4.png)
- **Trash**: ![Trash](/assets/trash/Trash1.png) ![Trash](/assets/trash/Trash2.png) ![Trash](/assets/trash/Trash3.png)
- **Database**: ![Database](/assets/db/psql1.png) ![Database](/assets/db/psql2.png) ![Database](/assets/db/psql3.png) ![Database](/assets/db/psql4.png) ![Database](/assets/db/psql5.png)

## Sample Data
It is possible in PostgreSQL: 
```
-- Insert data into the employees table
INSERT INTO employees (name, department, hire_date)
VALUES 
('Alice Johnson', 'HR', '2020-05-15'),
('Bob Smith', 'IT', '2018-03-20'),
('Charlie Brown', 'Finance', '2019-07-10'),
('Diana White', 'IT', '2021-01-25'),
('Eve Black', 'Marketing', '2022-08-05');

-- Insert data into the grades table
INSERT INTO grades (employee_id, grade)
VALUES 
(1, 8.5),
(2, 9.2),
(3, 7.8),
(4, 6.5),
(5, 8.9);

-- Insert data into the projects table
INSERT INTO projects (id, title, description, start_date, end_date)
VALUES
(2, 'Cloud Migration', 'Migrate the company infrastructure to the cloud', '2023-01-01', '2023-06-30'),
(3, 'Budget Analysis', 'Perform a detailed analysis of company expenses', '2023-02-15', NULL),
(5, 'Marketing Campaign', 'Launch a new social media campaign', '2023-03-01', '2023-05-15');

INSERT INTO trash (employee_id, name, department, grade, hire_date)
VALUES 
(999, 'John Doe', 'Research', 7.5, '2021-12-01');
```
This is also possible by simply running our application and filling the table with this data through the application.

## UML Class Diagram
The UML class diagram provides a visual representation of the system’s structure, detailing the classes, attributes, methods, and their relationships.

![UML Diagram](UML/employeeperformanceapp3.png)

### Diagram Description:
- **Employee**: Represents employee details with attributes like `name`, `department`, and `hireDate`.
- **EmployeeGrade**: Extends `Employee` and adds an additional property `grade` to store the evaluation score.
- **EmployeeDAO**: Handles database operations for managing employees and grades.
- **EmployeeDAOInterface**: Interface for CRUD operations related to employee records.
- **HelloController**: JavaFX controller that handles UI interactions, including employee addition, modification, deletion, and evaluation.

## E-R Diagram

![E-R Diagram](E-R/E-R.png)

## Weekly Meeting Documentation
Weekly meeting summaries and action items can be found in the [Google Docs link](https://docs.google.com/document/d/1E4ld5ssIVgZshUG-lhLDjgzNAuSk3Rkg3Ik92CVwCgI/edit?usp=sharing).

## OOP Concepts and questions

### 1. **Encapsulation**
**Explanation:**  
Encapsulation is used to protect data by making fields private and providing public getter and setter methods to access and modify them.

**Code Example:**
```java
public class Employee {
    private final StringProperty name;
    private final StringProperty department;
    private final Date hireDate;
    private int id;

    public Employee(int id, String name, String department, Date hireDate) {
        this.id = id;
        this.name = new SimpleStringProperty(name);
        this.department = new SimpleStringProperty(department);
        this.hireDate = hireDate;
    }

    // Getter for name
    public String getName() {
        return name.get();
    }

    // Setter for name
    public void setName(String name) {
        this.name.set(name);
    }
}
```

### 2. **Access Modifiers**
**Explanation:**  
Access modifiers control the visibility of classes, methods, and variables. `private` hides the fields from outside, while `public` makes them accessible.

**Code Example:**
```java
public class EmployeeDAO {
    private final Connection connection;  // private access to the connection

    // public method accessible from outside
    public void addEmployee(Employee employee) {
        String query = "INSERT INTO employees (name, department, hire_date) VALUES (?, ?, ?)";
        try (PreparedStatement statement = connection.prepareStatement(query)) {
            statement.setString(1, employee.getName());
            statement.setString(2, employee.getDepartment());
            statement.setDate(3, new java.sql.Date(employee.getHireDate().getTime()));
            statement.executeUpdate();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}
```

### 3. **Constructor**
**Explanation:**  
Constructors are used to initialize objects with a valid state at the time of creation.

**Code Example:**
```java
public Employee(int id, String name, String department, Date hireDate) {
    this.id = id;
    this.name = new SimpleStringProperty(name);
    this.department = new SimpleStringProperty(department);
    this.hireDate = hireDate;
}
```

### 4. **Method Overloading**
**Explanation:**  
Method overloading allows multiple methods with the same name but different parameters, enabling the handling of different input types.

**Code Example:**
```java
public void addGrade(int employeeId, double grade) {
    // Add grade to employee
}

public void addGrade(EmployeeGrade employeeGrade) {
    // Add grade from EmployeeGrade object
}
```

### 5. **Exception Handling**
**Explanation:**  
Exception handling is used to manage errors, ensuring the application does not crash due to unexpected issues.

**Code Example:**
```java
try {
    Connection connection = DriverManager.getConnection("jdbc:postgresql://localhost:5432/postgres", "postgres", "123456");
} catch (SQLException e) {
    e.printStackTrace();
    showAlert("Database Error", "Could not connect to the database.");
}
```

### 6. **Inheritance**
**Explanation:**  
Inheritance allows a class (e.g., `EmployeeGrade`) to reuse properties and methods from a parent class (`Employee`).

**Code Example:**
```java
public class EmployeeGrade extends Employee {
    private double grade;

    public EmployeeGrade(int id, String name, String department, Date hireDate, double grade) {
        super(id, name, department, hireDate);  // Inherited constructor
        this.grade = grade;
    }
}
```

### 7. **Method Overriding**
**Explanation:**  
Method overriding allows subclasses to provide specific implementations of methods defined in a superclass.

**Code Example:**
```java
@Override
public String getName() {
    return super.getName();  // Overriding the getName method
}
```

### 8. **Interface**
**Explanation:**  
Interfaces define common behavior for classes to implement, ensuring consistency across different implementations.

**Code Example:**
```java
public interface EmployeeDAOInterface {
    void addEmployee(Employee employee);
    void updateEmployee(Employee employee);
}

public class EmployeeDAO implements EmployeeDAOInterface {
    @Override
    public void addEmployee(Employee employee) {
        // Implement add logic
    }

    @Override
    public void updateEmployee(Employee employee) {
        // Implement update logic
    }
}
```

### 9. **Polymorphism**
**Explanation:**  
Polymorphism allows the handling of objects of different types in a uniform way, typically through a common interface or superclass.

**Code Example:**
```java
List<Employee> employees = new ArrayList<>();
employees.add(new Employee(1, "John", "HR", new Date()));
employees.add(new EmployeeGrade(2, "Alice", "Engineering", new Date(), 85));

// Polymorphism in action
for (Employee e : employees) {
    System.out.println(e.getName());  // Works for both Employee and EmployeeGrade
}
```

### 10. **Dependency Injection**
**Explanation:**  
Dependency Injection reduces tight coupling by passing dependencies (e.g., `EmployeeDAO`) to a class rather than creating them inside.

**Code Example:**
```java
public class HelloController {
    private EmployeeDAO employeeDAO;

    // Constructor Injection
    public HelloController(EmployeeDAO employeeDAO) {
        this.employeeDAO = employeeDAO;
    }

    public void loadEmployeeData() {
        List<Employee> employees = employeeDAO.getAllEmployees();
        employeeTable.getItems().setAll(employees);
    }
}
```

## Unit Test Casesgit co

The EmployeeTest class includes three tests that validate the functionality of the Employee class:

    testGettersAndSetters: Verifies that the getters and setters for the employee’s attributes (ID, name, department, hire date) work as expected.
    testNameProperty: Tests the property functionality of the employee's name and ensures the name can be correctly updated.
    testDepartmentProperty: Tests the property functionality of the employee's department and ensures the department can be correctly updated.

The tests make use of JUnit 5 for structuring and validating the tests.
Test Cases
testGettersAndSetters

This test ensures that the employee's attributes can be correctly set and retrieved using getters and setters.

    Steps:
        An employee object is created with initial values for ID, name, department, and hire date.
        The getters are tested to ensure they return the correct values.
        The employee’s attributes are then updated using setters, and the getters are used again to confirm the updates.

testNameProperty

This test verifies the functionality of the employee's nameProperty() method and checks that the name can be correctly updated.

    Steps:
        An employee object is created.
        The employee's name is updated using setName().
        The nameProperty() method is used to verify that the property value reflects the change.

testDepartmentProperty

This test verifies the functionality of the employee's departmentProperty() method and checks that the department can be correctly updated.

    Steps:
        An employee object is created.
        The employee's department is updated using setDepartment().
        The departmentProperty() method is used to verify that the property value reflects the change.

Dependencies

    JUnit 5: The tests use the JUnit 5 framework for writing and executing the tests.


## Presentation
The project's presentation, I did with free platform "Canva", you can download presentation in PDF-format: [Canva Presentation](https://www.canva.com/design/DAGYJpr8GLQ/Qbxf5jwPTlJ-F0KIpi8T8Q/view?utm_content=DAGYJpr8GLQ&utm_campaign=designshare&utm_medium=link&utm_source=editor)


## GitHub Repository
The project source code and documentation can be accessed on GitHub at [GitHub Repository Link](https://github.com/EMMMABK/Employee-Performance-Evaluation-System.git).

## Jar File Build
Installation requirements:
1. https://gluonhq.com/products/javafx/ - JavaFX
2. https://www.oracle.com/java/technologies/downloads/?er=221886#jdk23-windows - Java Downloads
3. https://johann.loefflmann.net/en/software/jarfix/index.html - Jarfix

You need to provide the path to the JavaFX file




