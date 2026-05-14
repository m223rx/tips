# Challenge: Dockerized Multi‑Stage Web Application

## Difficulty
Medium

## Description
Create a Dockerized web application that serves a simple “Hello, World!” page. The application should be built using a **multi‑stage Docker build** to keep the final image lightweight. The source code can be written in any language/framework of your choice (e.g., Node.js, Python Flask, Go, etc.), but you must use at least two stages:

1. **Build stage** – compile or install dependencies.
2. **Runtime stage** – copy only the necessary artifacts from the build stage and run the application.

Your Docker image should expose port **8080** and be runnable with a single `docker run` command.

## Requirements
- Write a `Dockerfile` that implements a multi‑stage build.
- The final image size should be **significantly smaller** than the build image (e.g., < 100 MB for a typical Node.js/Python app).
- Include a `README.md` that explains how to:
  - Build the Docker image.
  - Run the container.
  - Verify that the application is reachable on `http://localhost:8080`.
- Use environment variables to configure the greeting message (default to “Hello, World!”) without rebuilding the image.
- Ensure the container runs as a **non‑root user**.

## Bonus
- Add a health‑check instruction in the Dockerfile that verifies the app returns a `200 OK` status.
- Create a `docker-compose.yml` file that launches the container and maps port 8080 automatically.
- Implement a small CI pipeline (e.g., GitHub Actions) that builds and pushes the Docker image to a container registry on every push to the `main` branch.