# Challenge: Dockerize a Simple Web Application

## Difficulty
Medium

## Description
You are tasked with containerizing a simple web application using Docker. The application consists of a backend API (written in a language of your choice) that serves JSON data and a static frontend that consumes this API. Your goal is to create a Docker setup that builds the application, runs it in a container, and makes it accessible on a specified port. Additionally, you should provide a `docker-compose.yml` file to orchestrate the services if you decide to split the frontend and backend into separate containers.

## Requirements
- Write a `Dockerfile` for the backend service that:
  - Uses an appropriate base image.
  - Installs any necessary dependencies.
  - Copies the source code into the container.
  - Exposes the correct port.
  - Defines a clean start-up command.
- Write a `Dockerfile` for the frontend service (if using a separate container) that:
  - Uses a lightweight web server (e.g., nginx, httpd) to serve static files.
  - Copies the built static assets into the appropriate directory.
- Create a `docker-compose.yml` file that:
  - Defines services for both the backend and frontend.
  - Links the frontend to the backend so that API calls succeed.
  - Maps container ports to host ports so the application is reachable at `http://localhost:<host_port>`.
- Provide a `README.md` with clear instructions on how to build and run the containers using Docker and Docker Compose.
- Ensure that the application runs correctly when the containers are started (the frontend should display data fetched from the backend).

## Bonus
- Implement multi-stage builds to minimize the final image sizes.
- Add environment variable support for configuring the backend API URL and the host ports.
- Set up health checks for both services in the `docker-compose.yml`.
- Use a reverse proxy (e.g., Traefik or nginx) in a separate container to route traffic to the frontend and backend based on URL paths.
- Write a simple CI/CD pipeline (e.g., using GitHub Actions) that builds and pushes the Docker images to a container registry on each commit.