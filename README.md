# CRUDDemo

## Description

CRUDDemo is a Spring Boot application that demonstrates basic Create, Read, Update, and Delete (CRUD) operations for managing employee data. The application uses Spring Data JPA for data access and MySQL as the database.

## Features

- Create, read, update, and delete employee records.
- RESTful API endpoints.
- Data validation using `javax.validation`.
- Exception handling for improved error management.

## Technologies Used

- **Java**: Programming language used for the application.
- **Spring Boot**: Framework for building the application.
- **Spring Data JPA**: For data persistence.
- **MySQL**: Database for storing employee records.
- **Lombok**: For reducing boilerplate code.

## Prerequisites

- JDK 21 or higher
- MySQL Database Server
- Maven
- Postman or any API testing tool

## Installation

1. **Clone the repository**:

   ```bash
   git clone <repository-url>
   cd demo
   ```

2. **Set up the MySQL Database**:

   - Create a database named `spring_crud`.
   - Update the `application.properties` file with your MySQL credentials.

3. **Run the application**:
   ```bash
   mvn spring-boot:run
   ```

## API Endpoints

### Employee API

- **Create Employee**

  - `POST /employees`
  - Request Body:
    ```json
    {
      "firstName": "John",
      "lastName": "Doe",
      "email": "john.doe@example.com",
      "phone": "1234567890",
      "salary": 50000,
      "department": "IT",
      "hireDate": "2024-01-01"
    }
    ```

- **Get All Employees**

  - `GET /employees`

- **Get Employee by ID**

  - `GET /employees/{id}`

- **Update Employee**

  - `PUT /employees/{id}`
  - Request Body:
    ```json
    {
      "firstName": "John",
      "lastName": "Smith",
      "email": "john.smith@example.com",
      "phone": "0987654321",
      "salary": 55000,
      "department": "HR",
      "hireDate": "2024-01-01"
    }
    ```

- **Delete Employee**
  - `DELETE /employees/{id}`

## Validation

The application uses validation annotations such as `@NotNull`, `@Size`, `@Email`, and `@Pattern` to enforce data integrity. If a validation error occurs, a descriptive message will be returned.

## Exception Handling

Global exception handling is implemented using `@ControllerAdvice` to manage exceptions consistently across the application.

## Testing the Application

You can test the API endpoints using Postman or any API testing tool of your choice.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

Sohel

```

### How to Use the README
- Replace `<repository-url>` with the URL of your GitHub repository.
- Update the author section with your name.
- Adjust any other sections as needed for your project.

Feel free to customize it further to fit your project!
```
