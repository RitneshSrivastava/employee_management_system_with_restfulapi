# Employee Management System

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.1.5-green)
![Java](https://img.shields.io/badge/Java-21-blue)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange)
![REST API](https://img.shields.io/badge/REST%20API-Yes-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

A Spring Boot application for managing employee records through a secure RESTful API. It supports CRUD operations, input validation, custom error handling, and MySQL integration.

Built to demonstrate backend fundamentals and clean API design: layered architecture, Spring Security Basic Authentication, persistence with Spring Data JPA, and database-backed employee management.

---

## Live Demo

**API Base URL:** `http://localhost:8080/api/employees`

> Local project only. No public deployment included yet.


---

## Features

### Employee Management
- Create, Read, Update, and Delete employee records
- Store employee details including first name, last name, email, department, position, and salary

### REST API
- RESTful CRUD endpoints
- Easy integration with frontend applications
- Tested using Postman

### Security
- Spring Security with Basic Authentication
- Protected REST endpoints

### Database
- MySQL persistence using Spring Data JPA and Hibernate

### Validation
- Bean Validation for employee data

### Error Handling
- Custom exception handling with meaningful API responses

---

## System Architecture

```text
                    Client / Postman
                            │
                            ▼
                     REST API (HTTP)
                            │
                            ▼
                  Spring Boot Backend
                            │
        ┌───────────────────┼───────────────────┐
        ▼                   ▼                   ▼
 Spring Security      Spring Data JPA        Hibernate
 (Basic Auth)             (MySQL)             (ORM)
                            │
                            ▼
                          MySQL
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Java 21, Spring Boot 3.1.5 |
| Security | Spring Security (Basic Authentication) |
| Persistence | Spring Data JPA, Hibernate, MySQL |
| Database | MySQL 8 |
| Testing | Postman |
| Build | Maven |
| Version Control | Git & GitHub |

---

## Project Structure

```text
employee_management_system_with_restfulapi/
├── src/
├── pom.xml
├── mvnw
└── README.md
```

---

## Getting Started (Local Development)

### Prerequisites

- Java 21
- MySQL
- Maven
- IntelliJ IDEA / Eclipse
- Postman

### Configure Database

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/employee_management
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### Run the Application

```bash
./mvnw spring-boot:run
```

The API will be available at:

```text
http://localhost:8080/api/employees
```

---

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/employees` | Get all employees |
| GET | `/api/employees/{id}` | Get employee by ID |
| POST | `/api/employees` | Create employee |
| PUT | `/api/employees/{id}` | Update employee |
| DELETE | `/api/employees/{id}` | Delete employee |

---

## Example Request

```json
{
  "firstName": "Priya",
  "lastName": "Patel",
  "email": "priya.patel@example.com",
  "department": "HR",
  "position": "HR Manager",
  "salary": 85000
}
```

---

## Design Decisions

### Why Spring Boot?
Provides a clean layered architecture and simplifies REST API development.

### Why Spring Data JPA?
Reduces boilerplate and makes persistence cleaner than raw JDBC.

### Why Basic Authentication?
Simple and appropriate for demonstrating Spring Security fundamentals.

### Why MySQL?
A reliable relational database that integrates seamlessly with Spring Data JPA.

---

## Roadmap / Future Enhancements

- JWT Authentication
- Swagger / OpenAPI
- Docker Support
- Pagination & Search
- Role-Based Access Control (RBAC)
- CI/CD Pipeline

---

## License

This project is licensed under the MIT License.

---

## Author

**Made with ❤️ by Ritnesh Kumar Srivastava**

- GitHub: https://github.com/RitneshSrivastava
- LinkedIn: https://www.linkedin.com/in/ritneshks
