
# 🎓 Student Management System API

A Spring Boot-based RESTful web service that manages student records. This system allows users to create, read, update, and delete (CRUD) student information using MySQL as the database.

## 🚀 Technologies Used

- Java 17+
- Spring Boot
- Spring Web
- Spring Data JPA (Hibernate)
- MySQL
- Maven
- Lombok
- Swagger (optional for API testing)

## 🏗️ Project Structure

```
student-management-system-api
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.example.student
│   │   │       ├── controller
│   │   │       ├── model
│   │   │       ├── repository
│   │   │       ├── service
│   │   │       └── StudentManagementApplication.java
│   │   └── resources
│   │       ├── application.properties
│   │       └── data.sql / schema.sql (if used)
└── pom.xml
```

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/student-management-system-api.git
cd student-management-system-api
```

### 2. Configure MySQL Database

Create a database in MySQL:

```sql
CREATE DATABASE student_db;
```

Then update your `application.properties` file:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_db
spring.datasource.username=root
spring.datasource.password=root
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 3. Build and Run the Project

Using terminal:

```bash
./mvnw clean install
./mvnw spring-boot:run
```

Or in IntelliJ IDEA:

- Open the project
- Run `StudentManagementApplication.java`

### 4. API Endpoints

| Method | Endpoint             | Description              |
|--------|----------------------|--------------------------|
| GET    | `/students`          | Get all students         |
| GET    | `/students/{id}`     | Get student by ID        |
| POST   | `/students`          | Add a new student        |
| PUT    | `/students/{id}`     | Update an existing student |
| DELETE | `/students/{id}`     | Delete a student         |

### 5. Testing

Use tools like **Postman** or **Swagger** for testing the API endpoints.

## ✅ Features

- Add a new student
- View all students
- Update student info
- Delete student record
- RESTful API design

## 🧪 Sample Request (JSON)

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com"
}
```

## 📌 Future Improvements

- Add pagination and sorting
- Add user authentication
- Integrate frontend (React/Angular)

## 🤝 Contribution

Feel free to fork this repo and raise a PR.

---

**Author:** RATHIK RAM POOJARY  
**License:** MIT
