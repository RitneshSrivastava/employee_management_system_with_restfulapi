# Employee Management System

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.1.5-green)
![Java](https://img.shields.io/badge/Java-21-blue)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange)
![REST API](https://img.shields.io/badge/REST%20API-Yes-brightgreen)

A **Spring Boot** application for managing employee records. This project demonstrates the implementation of a **RESTful API** with **CRUD operations**, **Spring Security**, and **MySQL database integration**. It is designed to be a professional and scalable solution for HR systems.

---

## Features

- **Employee Management**:
  - Create, Read, Update, and Delete (CRUD) employee records.
  - Store employee details such as name, email, department, position, and salary.
- **RESTful API**:
  - Fully documented REST API for seamless integration with front-end applications.
- **Security**:
  - Secure endpoints using **Spring Security** with **Basic Authentication**.
- **Database**:
  - **MySQL** database for persistent storage of employee records.
- **Validation**:
  - Input validation for employee data (e.g., email format, non-empty fields).
- **Error Handling**:
  - Custom exception handling with meaningful error messages.

---

## Technologies Used

- **Backend**: Spring Boot, Java 21
- **Database**: MySQL
- **Security**: Spring Security (Basic Authentication)
- **Build Tool**: Maven
- **API Testing**: Postman
- **Version Control**: Git

---

## Setup Instructions

### Prerequisites

1. **Java Development Kit (JDK)**: Ensure you have JDK 21 installed.
2. **MySQL**: Install and configure MySQL on your machine.
3. **IDE**: Use an IDE like IntelliJ IDEA or Eclipse.
4. **Postman**: For testing the REST API.

### Steps to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/RitneshSrivastava/employee-management-system.git
   cd employee-management-system
2.**Set Up the Database:**

  Create a MySQL database named employee_management.

  Update the application.properties file with your MySQL credentials:

  spring.datasource.url=jdbc:mysql://localhost:3306/your_databasename
  spring.datasource.username=your-username
  spring.datasource.password=your-password
  
3.**Run the Application:**

  Open the project in your IDE.
  Run the EmployeeManagementApplication.java file.
  
4.**Test the API:**

  -Use Postman or any API testing tool to test the endpoints.
5. **API Documentation**
     Base URL
    http://localhost:8080/api/employees
``Endpoints``
  ``HTTP Method	Endpoint	Description
  GET	/api/employees	Get all employees
  GET	/api/employees/{id}	Get an employee by ID
  POST	/api/employees	Create a new employee
  PUT	/api/employees/{id}	Update an employee by ID
  DELETE	/api/employees/{id}	Delete an employee by ID``

Example Requests
1. Get All Employees
URL: GET http://localhost:8080/api/employees

Response:

json

[
  {
    "id": 1,
    "firstName": "Rahul",
    "lastName": "Sharma",
    "email": "rahul.sharma@example.com",
    "department": "IT",
    "position": "Software Engineer",
    "salary": 75000.0
  }
]

2. Get Employee by ID
   
URL: GET http://localhost:8080/api/employees/1

Response:
{
  "id": 1,
  "firstName": "Rahul",
  "lastName": "Sharma",
  "email": "rahul.sharma@example.com",
  "department": "IT",
  "position": "Software Engineer",
  "salary": 75000.0
}
3. Create Employee

URL: POST http://localhost:8080/api/employees
{
  "firstName": "Priya",
  "lastName": "Patel",
  "email": "priya.patel@example.com",
  "department": "HR",
  "position": "HR Manager",
  "salary": 85000.0
}

Response:
{
  "id": 2,
  "firstName": "Priya",
  "lastName": "Patel",
  "email": "priya.patel@example.com",
  "department": "HR",
  "position": "HR Manager",
  "salary": 85000.0
}

4. Update Employee
   
URL: PUT http://localhost:8080/api/employees/1

{
  "firstName": "Rahul",
  "lastName": "Sharma",
  "email": "rahul.sharma@example.com",
  "department": "IT",
  "position": "Senior Software Engineer",
  "salary": 85000.0
}

Response:

{
  "id": 1,
  "firstName": "Rahul",
  "lastName": "Sharma",
  "email": "rahul.sharma@example.com",
  "department": "IT",
  "position": "Senior Software Engineer",
  "salary": 85000.0
}
5. Delete Employee
URL: DELETE http://localhost:8080/api/employees/1

The employees table has the following structure:

CREATE TABLE employees (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    department VARCHAR(100) NOT NULL,
    position VARCHAR(100) NOT NULL,
    salary DOUBLE NOT NULL
);
Security
Authentication: Basic Authentication

Username: admin

Password: admin123

Protected Endpoints: All endpoints under /api/employees are permitted.

Contributing
Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

Fork the repository.

Create a new branch (git checkout -b feature/YourFeatureName).

Commit your changes (git commit -m 'Add some feature').

Push to the branch (git push origin feature/YourFeatureName).

Open a pull request.

Contact
For any questions or feedback, feel free to reach out:

Name:Ritnesh Srivastava

Email:ritneshntv@gmail.com

LinkedIn:-https://www.linkedin.com/in/ritneshks

GitHub: https://github.com/RitneshSrivastava

Acknowledgments
Spring Boot: For providing a robust framework for building RESTful APIs.

MySQL: For reliable and scalable database management.

Postman: For simplifying API testing.

**Made with ❤️ by Ritnesh**
