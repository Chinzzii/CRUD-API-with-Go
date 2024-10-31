# Movie CRUD API

This is a simple CRUD (Create, Read, Update, Delete) API for managing movies, built with Go and the Gorilla Mux router.

## Features

- Get all movies
- Get a specific movie by ID
- Create a new movie
- Update an existing movie
- Delete a movie

## Prerequisites

- Go (version 1.x or later)
- Gorilla Mux package (`github.com/gorilla/mux`)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Chinzzii/CRUD-API-with-Go
   cd CRUD-API-with-Go
   ```

2. Install the Gorilla Mux package:
   ```bash
   go get -u github.com/gorilla/mux
   ```

4. Run the server:
   ```bash
   go run main.go
   ```

The server will start on `http://localhost:8000`.

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | /movies  | Get all movies |
| GET    | /movies/{id} | Get a specific movie |
| POST   | /movies  | Create a new movie |
| PUT    | /movies/{id} | Update a movie |
| DELETE | /movies/{id} | Delete a movie |

## Data Model

### Movie
```go
type Movie struct {
  ID       string    `json:"id"`
  Isbn     string    `json:"isbn"`
  Title    string    `json:"title"`
  Director *Director `json:"director"`
}
```

### Director
```go
type Director struct{
  Firstname string `json:"fristname"`
  Lastname string `json:"lastname"`
}
```
