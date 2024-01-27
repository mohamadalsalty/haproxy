# HAproxy app

## Introduction

This application sets up a basic web service using Docker with HAProxy as a load balancer and a web application server.

## Prerequisites

- Docker
- Docker Compose

## Running the Application

1. **Clone the Repository**: Clone or download the repository to your local machine.

2. **Navigate to the Application Directory**: Change to the directory containing the application files.

3. **Start the Services**: Run the following command to start the services defined in the docker-compose.yml file: </br>

    ```bash
    make up
    ```

   This command will start the HAProxy load balancer and the web application server in detached mode.

4. **Accessing the Application**: The web application can be accessed at `http://localhost`.

5. **HAProxy Statistics**: Access HAProxy statistics at `http://localhost/haproxy?stats`.

## Components

- **HAProxy**: A high availability load balancer and proxy server for TCP and HTTP-based applications. It's configured to balance the load between instances of the web application.
- **Web Application (httpd)**: A simple HTTP server running the Apache HTTP Server (`httpd`).

## Configuration Files

- `Makefile`: Contains commands to manage the application with Docker Compose.
- `haproxy.cfg`: Configuration file for HAProxy.
- `docker-compose.yml`: Defines the services, networks, and volumes for Docker containers.
