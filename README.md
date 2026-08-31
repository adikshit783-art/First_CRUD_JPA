# First_CRUD_JPA
first project perfoming CRUD operation on MYSQL student database


# Student Management System – CRUD API

A simple **Student Management REST API** built using **Java, Spring Boot, Spring Data JPA, Hibernate, and MySQL**.

This project demonstrates the basic **CRUD (Create, Read, Update, Delete)** operations using JPA to interact with a MySQL database.

## 🚀 Features

* Create a new student
* Get all students
* Get a student by ID
* Update student details
* Delete a student
* MySQL database integration
* Spring Data JPA for database operations
* RESTful APIs

## 🛠️ Technologies Used

* **Java**
* **Spring Boot**
* **Spring Web**
* **Spring Data JPA**
* **Hibernate**
* **MySQL**
* **Maven**
* **Postman** – API testing

## 📂 Project Structure

```text
src/main/java
└── com.practice.jpa.First
    ├── Controller
    │   └── StudentController.java
    │
    ├── Service
    │   └── StudentService.java
    │
    ├── Repository
    │   └── StudentRepository.java
    │
    └── entity
        └── Student.java
```

## 🗄️ Database Configuration

Create a MySQL database:

```sql
CREATE DATABASE studentdb;
```

Configure the database in `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/studentdb
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

Replace `YOUR_PASSWORD` with your MySQL password.

## 🔗 API Endpoints

### Create Student

```http
POST /Student/Save
```

Request Body:

```json
{
    "rollno": 101,
    "name": "Shivam",
    "email": "shivam@example.com"
}
```

### Get All Students

```http
GET /Student/All
```

### Get Student By ID

```http
GET /Student/{id}
```

### Update Student

```http
PUT /Student/{id}
```

### Delete Student

```http
DELETE /Student/{id}
```

> The exact endpoint names may vary depending on your controller implementation.

## 🔄 CRUD Operations

| Operation | HTTP Method | Purpose               |
| --------- | ----------- | --------------------- |
| Create    | POST        | Add a new student     |
| Read      | GET         | Retrieve student data |
| Update    | PUT         | Modify student data   |
| Delete    | DELETE      | Remove a student      |

## 🧩 How It Works

The application follows a simple layered architecture:

```text
Client
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
JPA / Hibernate
   ↓
MySQL
```

### Controller

Handles HTTP requests and responses.

### Service

Contains the application's business logic.

### Repository

Uses `JpaRepository` to perform database operations without manually writing SQL for basic CRUD operations.

### Entity

Represents the `Student` table in the MySQL database.

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Open the project

Open the project in **IntelliJ IDEA** or your preferred Java IDE.

### 3. Configure MySQL

Create the database and update the database credentials in:

```text
src/main/resources/application.properties
```

### 4. Run the application

Run the main Spring Boot application class.

The application will start on:

```text
http://localhost:8080
```

### 5. Test the APIs

Use **Postman** or any REST API client to test the CRUD endpoints.

## 📚 Concepts Demonstrated

This project demonstrates:

* Spring Boot fundamentals
* REST API development
* Dependency Injection
* Layered architecture
* JPA
* Hibernate
* `JpaRepository`
* Entity mapping
* MySQL integration
* CRUD operations
* HTTP methods
* JSON request/response handling

## 🔮 Future Improvements

* Add DTOs
* Add input validation
* Add global exception handling
* Add Spring Security
* Add JWT authentication
* Add pagination and sorting
* Add Swagger/OpenAPI documentation
* Add unit and integration tests

## 👨‍💻 Author

**ABHISHEK**

Java Backend Developer | Spring Boot | JPA | MySQL | REST APIs
