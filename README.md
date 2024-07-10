# go-REST-API-MongoDB

A simple RESTful API built with Go and MongoDB.

## Overview

This project demonstrates how to build a basic REST API using Go and MongoDB. The API allows you to create, read, and delete user records.

### main.go

The main entry point of the application. It sets up the HTTP server and the routes for the API.

### controllers/user.go

Contains the logic for handling the API requests and responses. It includes functions for creating, reading, and deleting users.

### models/user.go

Defines the User model and its structure.

## Endpoints

- `GET /user/:id` - Retrieve a user by their ID.
- `POST /user` - Create a new user.
- `DELETE /user/:id` - Delete a user by their ID.

## Getting Started

### Prerequisites

- Go (1.16 or higher)
- MongoDB

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/aryanraw/go-REST-API-MongoDB.git
    cd go-REST-API-MongoDB
    ```

2. Install dependencies:

    ```bash
    go mod download
    ```

3. Run MongoDB server locally (if not already running):

    ```bash
    mongod --dbpath /path/to/your/mongodb/data
    ```

4. Run the application:

    ```bash
    go run main.go
    ```

The server will start on `localhost:9000`.

### Usage

#### Create a User

```bash
curl -X POST -H "Content-Type: application/json" -d '{"name":"John Doe", "gender":"male", "age":30}' http://localhost:9000/user
```

#### Get a User

```bash
curl http://localhost:9000/user/{id}
```

#### Delete a User

```bash
curl -X DELETE http://localhost:9000/user/{id}
```
