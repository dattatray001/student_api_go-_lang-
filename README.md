# Student REST API (Go)

A simple and clean RESTful API built with Go (Golang) for managing student data.  
This project follows a clean architecture approach with proper separation of concerns and uses SQLite as the database.

---

## Features

- RESTful API design
- CRUD operations for Students
- SQLite database integration
- Clean architecture (handlers, services, storage)
- Configurable via YAML
- Ready-to-use Postman collection
- Lightweight and fast

---

## Tech Stack

- **Language:** Go (Golang)
- **Framework:** net/http
- **Database:** SQLite
- **Config:** YAML
- **Dependency Management:** Go Modules

---

## Project Structure

```
REST_API/
│
├── cmd/
│   └── studen-api/
│       └── main.go
│
├── config/
│   └── local.yaml
│
├── internal/
│   ├── config/
│   ├── http/
│   │   └── handlers/
│   │       └── student/
│   ├── storage/
│   │   ├── sqlite/
│   │   └── storage.go
│   ├── types/
│   └── utils/
│       └── response/
│
├── storage/
│   └── storage.db
│
├── Students_API_Postman_Collection.json
├── go.mod
├── go.sum
└── README.md
```

---

## Configuration

Configuration file location:

```
config/local.yaml
```

Example:

```yaml
env: local
storage_path: storage/storage.db
http_server:
  address: "localhost:8080"
  timeout: 4s
  idle_timeout: 60s
```

---

## How to Run the Project

### Prerequisites

- Go 1.20+
- Git

---

### Clone the Repository

```bash
git clone https://github.com/dattatray001/student_api_go-_lang-.git
cd REST_API
```

---

### Install Dependencies

```bash
go mod tidy
```

---

### Run the Application

```bash
go run cmd/studen-api/main.go
```

Server starts at:

```
http://localhost:8080
```

---

## API Endpoints

| Method | Endpoint       | Description       |
| ------ | -------------- | ----------------- |
| POST   | /students      | Create student    |
| GET    | /students      | Get all students  |
| GET    | /students/{id} | Get student by ID |
| PUT    | /students/{id} | Update student    |
| DELETE | /students/{id} | Delete student    |

---

## API Testing

Postman collection included:

```
Students_API_Postman_Collection.json
```

Steps:

1. Open Postman
2. Import the collection
3. Test APIs

---

## Database

- **Database:** SQLite
- **Location:** `storage/storage.db`

---

## Architecture Overview

- Handlers manage HTTP requests and responses
- Storage layer uses interfaces for abstraction
- Config layer handles environment configuration
- Utils provide common API responses

---

## Future Enhancements

- JWT authentication
- Input validation
- Pagination & filtering
- Docker support
- Swagger / OpenAPI

---

## Author

**Dattatray Narhe**
