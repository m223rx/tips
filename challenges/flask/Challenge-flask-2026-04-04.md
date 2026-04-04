# Challenge: Flask Personal Diary API

## Difficulty
Medium

## Description
Create a small web service using Flask that allows a user to manage personal diary entries. The application should expose a JSON API to create, read, update, and delete entries. Each diary entry must contain a title, body text, a timestamp, and an optional list of tags. Users must authenticate before they can access any endpoint, and each user should only be able to see and modify their own entries.

## Requirements
- Set up a Flask project with a clear project structure.
- Use **SQLite** (or any other lightweight relational database) together with **SQLAlchemy** for data storage.
- Implement **user registration** and **login** endpoints. Store passwords securely (e.g., using hashing).
- Protect all diary‑related endpoints with token‑based authentication (e.g., JWT or Flask‑Login sessions).
- Provide the following CRUD API endpoints for diary entries:
  - `POST /entries` – Create a new entry.
  - `GET /entries` – List all entries belonging to the authenticated user.
  - `GET /entries/<id>` – Retrieve a specific entry.
  - `PUT /entries/<id>` – Update an existing entry.
  - `DELETE /entries/<id>` – Delete an entry.
- Each entry must contain:
  - `title` (string, required)
  - `body` (string, required)
  - `timestamp` (automatically set on creation, immutable)
  - `tags` (list of strings, optional)
- Return proper HTTP status codes and JSON responses for success and error cases.
- Validate input data and handle common error scenarios (e.g., missing fields, unauthorized access, non‑existent IDs).

## Bonus
- Add **pagination** and **filtering** capabilities to the `GET /entries` endpoint (e.g., page size, page number, filter by tag).
- Implement a **search** endpoint that allows users to search their entries by keyword in the title or body.
- Write a suite of **unit tests** for the API using `pytest` and `Flask-Testing`.
- Containerize the application with a **Dockerfile** and provide a `docker-compose.yml` that includes the database.
- Deploy the app to a free hosting platform (e.g., Heroku, Render) and provide the live URL.