# FastAPI Boilerplate

## Purpose

This document defines the standard FastAPI boilerplate used to initialize new backend applications.

The boilerplate provides a production-ready foundation that follows the FastAPI architecture and engineering standards defined by this framework.

This document describes the components that should exist in a newly scaffolded project.

---

# Objective

Every generated FastAPI project should:

- be production-ready
- be immediately runnable
- follow the FastAPI architecture
- provide a consistent developer experience
- minimize manual setup

---

# Project Structure

Generate the following project structure.

```text
app/
├── api/
│   ├── dependencies.py
│   ├── responses.py
│   └── router.py
│
├── core/
│   ├── config.py
│   ├── constants.py
│   ├── database.py
│   ├── lifespan.py
│   ├── logging.py
│   └── security.py
│
├── db/
│   ├── base.py
│   ├── session.py
│   └── models/
│
├── exceptions/
│   ├── base.py
│   ├── handlers.py
│   ├── http.py
│   └── validation.py
│
├── features/
│   ├── __init__.py
│   └── health/
│
├── middleware/
│   ├── cors.py
│   ├── logging.py
│   └── request_id.py
│
├── shared/
│   ├── enums.py
│   ├── pagination.py
│   ├── responses.py
│   ├── types.py
│   ├── utils.py
│   └── validators.py
│
└── main.py

alembic/
tests/

.github/
└── workflows/

.env
.env.example
.gitignore
.dockerignore
Dockerfile
docker-compose.yml
alembic.ini
Makefile
pyproject.toml
README.md
```

---

# Initial Features

The boilerplate should include only one feature.

```text
health/
```

The purpose of this feature is to verify that the application is operational.

Do not generate additional business features.

---

# Health Endpoint

The Health feature should expose

```
GET /health
```

The endpoint should return a simple success response indicating that the application is running.

---

# API

The generated application should include:

- FastAPI application
- API versioning
- Central router
- OpenAPI support

The API should be mounted under

```
/api/v1
```

---

# Configuration

The project should provide centralized configuration.

Configuration should use:

- Pydantic Settings
- `.env`
- `.env.example`

Configuration should never be scattered throughout the project.

---

# Database

The project should include:

- SQLAlchemy
- Async Engine
- Async Session
- Declarative Base
- Alembic

The project should not generate application-specific models.

---

# Logging

Provide centralized logging.

The logging configuration should be reusable across the application.

Avoid using `print()`.

---

# Middleware

Include middleware for:

- CORS
- Request Logging
- Request ID

Only include middleware required by nearly every application.

---

# Exception Handling

Provide centralized exception handling.

Support:

- HTTP exceptions
- Validation exceptions
- Application exceptions

Feature-specific exceptions belong inside each feature.

---

# Testing

Create the standard testing structure.

```text
tests/
├── api/
├── integration/
├── unit/
└── conftest.py
```

Do not generate example tests beyond validating the Health endpoint.

---

# Development Tooling

Configure the project with:

- Ruff
- Pytest
- Docker
- Docker Compose
- GitHub Actions

Do not include additional tooling unless requested.

---

# Dependencies

Include only the dependencies required for a production-ready FastAPI application.

Avoid optional packages.

Do not include:

- Redis
- Celery
- RabbitMQ
- Kafka
- Authentication providers
- Cloud SDKs
- Background workers
- Monitoring frameworks
- Metrics frameworks

These should be added only when required by the application.

---

# Documentation

Generate a README that includes:

- Project overview
- Installation
- Environment variables
- Running locally
- Running with Docker
- Running tests
- Project structure

---

# Guiding Philosophy

The boilerplate should remain intentionally minimal.

It should provide everything required to begin application development without including functionality that every project may not need.

The boilerplate should serve as a clean foundation that developers extend according to the requirements of their application.