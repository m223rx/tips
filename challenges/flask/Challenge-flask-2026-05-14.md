# Challenge: Build a Simple Flask Todo API

## Difficulty
Medium

## Description
Create a small web service using Flask that allows users to manage a list of todo items. The API should support creating, reading, updating, and deleting (CRUD) todo entries. Data can be stored in memory (e.g., a Python list or dictionary); persistence across server restarts is not required.

## Requirements
- Use Flask to set up the web server.
- Implement the following endpoints:
  - `GET /todos` – Return a JSON array of all todo items.
  - `GET /todos/<int:id>` – Return a single todo item by its ID.
  - `POST /todos` – Create a new todo item. Expect a JSON payload with at least a `"title"` field. Return the created item with its assigned ID.
  - `PUT /todos/<int:id>` – Update an existing todo item. Accept a JSON payload that can modify the `"title"` and/or a `"completed"` boolean flag.
  - `DELETE /todos/<int:id>` – Remove a todo item by ID.
- Each todo item should have the following structure:
  ```json
  {
    "id": <int>,
    "title": "<string>",
    "completed": <bool>
  }
  ```
- Return appropriate HTTP status codes (e.g., 200 for success, 201 for creation, 404 for not found, 400 for bad requests).
- Validate input data and handle error cases gracefully with meaningful error messages in JSON format.

## Bonus
- Implement pagination for the `GET /todos` endpoint (e.g., `?page=1&limit=10`).
- Add support for filtering todos by their completion status (e.g., `?completed=true`).
- Persist data to a simple file (e.g., JSON) so that todo items survive server restarts.
- Include basic authentication (e.g., API key passed in a header) to protect the endpoints.