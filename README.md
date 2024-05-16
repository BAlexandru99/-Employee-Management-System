# Employee Management System

This Spring Boot application provides a CRUD (Create, Read, Update, Delete) API for managing employees. The application leverages Spring Security for role-based access control and uses an in-memory database for storing user details.

## Features

- **CRUD Operations**: Create, read, update, and delete employee records.
- **Role-Based Security**:
  - **EMPLOYEE role**: Can view employee details.
  - **MANAGER role**: Can add and update employee records.
  - **ADMIN role**: Can delete employee records.
- **RESTful Endpoints**: Expose endpoints to interact with employee data.
- **In-Memory User Storage**: Pre-defined users with specific roles for testing purposes.

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 11 or higher
- Maven

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/employee-management-system.git
    ```
2. Navigate to the project directory:
    ```bash
    cd employee-management-system
    ```
3. Build the project:
    ```bash
    mvn clean install
    ```
4. Run the application:
    ```bash
    mvn spring-boot:run
    ```

## Default Users

- **john (Role: EMPLOYEE)**
  - Username: `john`
  - Password: `test123`
- **mary (Roles: EMPLOYEE, MANAGER)**
  - Username: `mary`
  - Password: `test123`
- **susan (Roles: EMPLOYEE, MANAGER, ADMIN)**
  - Username: `susan`
  - Password: `test123`

## API Endpoints

- **Get All Employees**
  ```http
  GET /api/employees
Roles: EMPLOYEE, MANAGER, ADMIN

-**Get Employee by ID**



* GET /api/employees/{employeeId}
Roles: EMPLOYEE, MANAGER, ADMIN
Add New Employee



* POST /api/employees
Roles: MANAGER, ADMIN
Update Employee



* PUT /api/employees
Roles: MANAGER, ADMIN
Delete Employee



* DELETE /api/employees/{employeeId}
Roles: ADMIN
Security Configuration
The application uses HTTP Basic authentication and disables CSRF protection for simplicity in handling REST API requests.

- **Project Structure**
* com.luv2code.springboot.cruddemo.security: Security configuration classes.
* com.luv2code.springboot.cruddemo.service: Service layer interfaces and implementations.
* com.luv2code.springboot.cruddemo.rest: REST controller classes for handling API requests.
* com.luv2code.springboot.cruddemo.entity: Entity classes representing the database tables.
* com.luv2code.springboot.cruddemo.dao: Repository interfaces for data access.
