# FastAPI Architecture

## Purpose

This document defines the recommended architecture for FastAPI applications created using this framework.

It establishes a consistent structure that promotes maintainability, scalability, and readability while avoiding unnecessary complexity.

This document describes **what** the architecture should be. It does not describe **how** to implement it.

---

# Objective

Every FastAPI application should:

- follow a consistent architecture
- separate responsibilities clearly
- be easy to understand
- be easy to extend
- be production-ready
- remain maintainable as the project grows

---

# Design Principles

The architecture follows these principles.

- Feature-first organization.
- Thin routers.
- Business logic belongs in services.
- Database access belongs in repositories.
- Explicit dependency flow.
- Explicit route registration.
- Single responsibility per file.
- Composition over inheritance.
- Readability over cleverness.
- Simplicity over unnecessary abstraction.

---

# Project Structure

Every FastAPI project should follow this structure.

```text
app/
├── api/
├── core/
├── db/
├── exceptions/
├── features/
├── middleware/
├── shared/
└── main.py
```

Each top-level directory has a single responsibility.

---

# Feature Organization

Applications are organized by feature.

Each feature owns its own implementation.

Example

```text
features/
├── auth/
├── users/
├── clients/
├── invoices/
└── health/
```

Features should remain independent whenever practical.

---

# Feature Structure

Every feature follows the same structure.

```text
feature/
├── __init__.py
├── router.py
├── service.py
├── repository.py
├── schemas.py
├── exceptions.py
└── dependencies.py
```

Additional files may be introduced only when required by the feature.

Examples

- validators.py
- constants.py
- permissions.py
- tasks.py

Do not create unnecessary files.

---

# Layer Responsibilities

## Router

Responsible for

- HTTP endpoints
- request validation
- response serialization
- calling services

Must not contain

- business logic
- SQL
- persistence

---

## Service

Responsible for

- business logic
- application workflows
- coordinating repositories

Must not

- access HTTP request objects
- return HTTP responses
- execute SQL

---

## Repository

Responsible for

- persistence
- CRUD operations
- database queries

Must not

- implement business rules
- return HTTP responses

---

## Schemas

Responsible for

- request models
- response models
- validation models

---

## Dependencies

Responsible for

- feature-specific dependency injection

---

## Exceptions

Responsible for

- feature-specific exceptions

---

# Routing

Each feature owns its own router.

Every router must be registered centrally.

Example

```text
main.py
        │
        ▼
api/router.py
        │
        ▼
feature.router
```

Automatic route discovery should not be used.

Route registration should always be explicit.

---

# Feature Registration

Each feature exposes its router.

Example

```python
from .router import router

__all__ = ["router"]
```

Internal modules should not be exported.

---

# Database Organization

Database models belong under

```text
app/db/models/
```

Repositories interact with these models.

Features do not own database models.

---

# Dependency Flow

Dependencies always flow in one direction.

```text
Router
    │
    ▼
Service
    │
    ▼
Repository
    │
    ▼
Database
```

Reverse dependencies should be avoided.

---

# Shared Components

Common functionality belongs inside

```text
app/shared/
```

Examples include

- pagination
- response models
- enums
- validators
- utility functions

Only functionality reused across multiple features belongs here.

---

# Core Components

Application-wide infrastructure belongs inside

```text
app/core/
```

Examples include

- configuration
- database configuration
- logging
- security
- application lifecycle
- constants

---

# Middleware

Cross-cutting concerns belong inside

```text
app/middleware/
```

Examples include

- CORS
- request logging
- request IDs

---

# Exceptions

Shared exception handling belongs inside

```text
app/exceptions/
```

Feature-specific exceptions remain inside their respective feature.

---

# Guiding Philosophy

This architecture intentionally favors consistency over flexibility.

Developers should extend the existing architecture rather than introducing new patterns.

When multiple implementations are possible:

- choose the simplest solution
- preserve consistency
- follow existing project patterns
- avoid unnecessary abstraction

The architecture should remain understandable to any engineer joining the project with minimal onboarding.