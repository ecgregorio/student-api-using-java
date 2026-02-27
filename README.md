# Student API

A simple RESTful CRUD API for managing student records, built with **Spring Boot** and backed by an **H2 in-memory database**.

## Endpoints

| Method | Path             | Description              | Status |
|--------|------------------|--------------------------|--------|
| GET    | `/students`      | Retrieve all students    | 200    |
| GET    | `/students/{id}` | Retrieve a student by ID | 200    |
| POST   | `/students`      | Create a new student     | 201    |
| PUT    | `/students/{id}` | Update an existing student | 200  |
| DELETE | `/students/{id}` | Delete a student         | 200    |

## Request Body (POST / PUT)

```json
{
  "name": "Jane Doe",
  "age": 20,
  "course": "Computer Science"
}
```

All fields are required. `name` and `course` must not be blank; `age` must be 0 or greater.

## Running the Application

```bash
./mvnw spring-boot:run
```

The API will be available at `http://localhost:8080`.

### H2 Console

An in-browser H2 console is available at `http://localhost:8080/h2-console` while the application is running.

- **JDBC URL**: `jdbc:h2:mem:studentsdb`
- **Username**: `sa`
- **Password**: *(leave blank)*

## Running Tests

```bash
./mvnw test
```

## Tech Stack

- Java 21
- Spring Boot 4
- Spring Data JPA
- H2 Database (in-memory)
- Bean Validation (Jakarta)
