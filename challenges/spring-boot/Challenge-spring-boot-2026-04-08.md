# Challenge: Build a Simple Todo REST API with Spring Boot

## Difficulty
Medium

## Description
Create a RESTful web service using **Spring Boot** that manages a list of todo items. The service should allow clients to create, read, update, and delete (CRUD) todo entries. Data can be stored in an in‑memory data structure (e.g., a `List` or `Map`) or using an embedded database such as H2.

## Requirements
- **Project Setup**
  - Initialize a Spring Boot project (Maven or Gradle) with the following dependencies:
    - Spring Web
    - Spring Data JPA (if you choose to use a database)
    - H2 Database (optional, for persistence)
    - Validation (`spring-boot-starter-validation`)

- **Todo Model**
  - Create a `Todo` entity with at least the following fields:
    - `id` (Long, auto‑generated)
    - `title` (String, not blank)
    - `description` (String, optional)
    - `completed` (boolean, default `false`)

- **API Endpoints**
  - `GET /api/todos` – Return a list of all todo items.
  - `GET /api/todos/{id}` – Return a single todo item by its ID. Return **404** if not found.
  - `POST /api/todos` – Create a new todo item. Validate the request body, return **201** with the created resource.
  - `PUT /api/todos/{id}` – Update an existing todo item entirely. Return **404** if the item does not exist.
  - `PATCH /api/todos/{id}` – Partially update an existing todo (e.g., only toggle `completed`). Return **404** if not found.
  - `DELETE /api/todos/{id}` – Remove a todo item. Return **204** on success.

- **Validation & Error Handling**
  - Use Bean Validation annotations to enforce non‑blank titles.
  - Return meaningful error responses (JSON) for validation failures and missing resources.

- **Testing**
  - Write unit tests for the service layer.
  - Write integration tests for the controller endpoints using `@SpringBootTest` or `MockMvc`.

## Bonus
- Implement pagination and sorting for the `GET /api/todos` endpoint.
- Add a query parameter to filter todos by their completion status, e.g., `GET /api/todos?completed=true`.
- Secure the API with basic authentication or JWT.
- Persist data using a relational database (PostgreSQL, MySQL) instead of H2, and include migration scripts (Flyway or Liquibase).
- Dockerize the application and provide a `docker-compose.yml` that runs the Spring Boot app together with the chosen database.