# Task Management API

A simple Task Management REST API built with FastAPI.

## Features

- Create, Read, Update, Delete tasks
- SQLite database
- SQLAlchemy ORM
- Pydantic validation
- JWT Authentication
- Swagger API documentation

## Setup

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload
```

## Project Structure

```text
task-manager-api/
│
├── main.py
├── database.py
├── models.py
├── schemas.py
├── crud.py
├── auth.py
├── requirements.txt
└── README.md
```

## API Documentation

Open in browser:

```text
http://127.0.0.1:8000/docs
```

## Authentication APIs

### Register User

**POST**

```text
http://127.0.0.1:8000/register?username=rahul&password=123456
```

Use this API to create a new user account.

### Login User

**POST**

```text
http://127.0.0.1:8000/login?username=rahul&password=123456
```

Use this API to login and generate a JWT access token.

### Get Current User

**GET**

```text
http://127.0.0.1:8000/me
```

Use this API with a Bearer token to get the currently logged-in user.

---

## Task Management APIs

### Create Task

**POST**

```text
http://127.0.0.1:8000/tasks
```

Create a new task.

### Get All Tasks

**GET**

```text
http://127.0.0.1:8000/tasks
```

Retrieve all tasks.

### Get Task By ID

**GET**

```text
http://127.0.0.1:8000/tasks/1
```

Retrieve a specific task by its ID.

### Update Task

**PUT**

```text
http://127.0.0.1:8000/tasks/1
```

Update an existing task.

### Delete Task

**DELETE**

```text
http://127.0.0.1:8000/tasks/1
```

Delete a task by its ID.