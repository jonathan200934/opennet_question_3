# Greeting API

A simple RESTful API built with Flask that provides a greeting endpoint. This project demonstrates basic API development with Flask, containerization with Docker.

## Project Structure

```
opennet_question_3/
├── app.py              # Main Flask application
├── requirements.txt    # Python dependencies
├── Dockerfile         # Container configuration
├── docker-compose.yml # Docker Compose configuration
└── README.md         # Project documentation
```

## Prerequisites

- Python 3.11 or higher
- Docker and Docker Compose (optional, for containerized deployment)
- pip (Python package manager)

## Installation and Setup

### Running with Docker Compose (Recommended)

1. Clone the repository:
```bash
git clone <repository-url>
cd opennet_question_3
```

2. Build and run the containers:
```bash
docker-compose up --build
```

The API will be available at `http://localhost:8080`

![Kapture 2025-02-16 at 16 14 40](https://github.com/user-attachments/assets/f48ebbb2-dc74-4775-abc9-147cc7ba0f74)


## API Documentation

### Endpoint: GET /greet

Returns a greeting message. Can be customized with a name parameter.

#### Query Parameters

- `name` (optional): The name to include in the greeting

#### Response Format

```json
{
    "message": "Hello, {name}!"
}
```

#### Examples

1. Default greeting:
```bash
curl http://localhost:5000/greet
```
Response:
```json
{
    "message": "Hello, World!"
}
```

2. Custom greeting:
```bash
curl http://localhost:5000/greet?name=Alice
```
Response:
```json
{
    "message": "Hello, Alice!"
}
```
