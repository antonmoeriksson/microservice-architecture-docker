# API for a Task Application
This is a backend for managing a simple task management application.
The backend consists of three different parts:

- Go server application
- PostgreSQL
- NGINX

# Building & Running
Dependencies: 
* Docker 18.03.1-ce, build 9ee9f4
* PostgreSQL 9.5.12
* Nginx 1.10.3

The project can be built and run with the following commands:

## 1. PostgreSQL Database:
`docker build --no-cache -t postgres .`

`docker run --rm --name=postgres_db --net=testnet postgres:latest`

## 2. Go Server:
`docker build --no-cache -t go-server .`

`docker run --rm --name=server --net=testnet go-server:latest`

## 3. Nginx:
`docker build --no-cache -t nginx .`

`docker run --rm --name=nginx --net=testnet -p=30000:80 nginx:latest`

# Testing
The system can be tested by running `go test` in the application folder.
This requires the database to be running.

# Credits
Code skeleton adapted from TDDE06, Dockerized and configured as a microservice architecture.
