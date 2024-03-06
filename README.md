# Dockerized Full Stack Application Setup with Nginx Proxy

This guide outlines how to set up a full-stack application using Docker containers. We utilize Nginx as a reverse proxy to serve the front-end and route API requests to the back-end. Docker Compose is used to define and run multi-container Docker applications.

## Prerequisites

- Docker installed on your machine.
- Docker Compose installed on your machine.
- Basic knowledge of Docker, Nginx, and your front-end/back-end technologies.

## Structure Overview

- `front-end/`: Directory containing the front-end code.
- `back-end/`: Directory containing the back-end code.
- `proxy/`: Directory containing Nginx configuration for routing.
- `docker-compose.yml`: Docker Compose file to orchestrate the containers.

## Setup Steps

1. **Prepare Application Directories**
   Create directories for your front-end and back-end applications, and place your code accordingly.

2. **Create Dockerfiles**
   - **Front-end Dockerfile**: In the `front-end/` directory, create a `Dockerfile` to build your front-end image.
   - **Back-end Dockerfile**: In the `back-end/` directory, create a `Dockerfile` to build your back-end image.

3. **Configure Nginx as a Proxy**
   - In the `proxy/` directory, create a `Dockerfile` for the Nginx image and a `proxy.conf` file for the Nginx configuration.
   - The `proxy.conf` should define routing rules for your front-end and API endpoints.

4. **Define Services in Docker Compose**
   Create a `docker-compose.yml` at the root of your project. Define services for the front-end, back-end, and proxy. Ensure the proxy service routes traffic to the other services.

5. **Build and Run Containers**
   Run `docker-compose up --build` to build and start your containers.
