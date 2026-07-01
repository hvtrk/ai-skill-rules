# FastAPI Feature Structure

## Purpose

This document defines the standard structure for implementing features within a FastAPI application.

Every feature should follow the same organization to ensure consistency, maintainability, and predictable development across the project.

This document describes how features should be organized. It does not define feature-specific business logic.

---

# Objective

Every feature should:

- follow a consistent structure
- encapsulate its own functionality
- expose a single public router
- separate business logic from HTTP handling
- isolate persistence from business logic
- remain independent of other features whenever practical

---

# Feature Structure

Every feature must follow this structure.

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

This structure should remain consistent across all features.

---

# Optional Files

Additional files may be introduced only when required.

Examples include:

```text
constants.py
permissions.py
validators.py
tasks.py
```

Do not create files that are not needed.

---

# Public Interface

Every feature exposes exactly one public object.

```python
from .router import router

__all__ = ["router"]
```

Internal implementation files should not be exported.

---

# Router

The router is responsible for HTTP communication.

Responsibilities:

- Define API endpoints.
- Validate incoming requests.
- Serialize responses.
- Call the appropriate service.

The router must not:

- Implement business logic.
- Access the database.
- Execute SQL.
- Perform complex processing.

Routers should remain thin.

---

# Service

The service contains the application's business logic.

Responsibilities:

- Implement business rules.
- Coordinate repositories.
- Coordinate multiple operations.
- Perform validation beyond request validation.

The service must not:

- Return HTTP responses.
- Access request objects.
- Execute SQL directly.

Services should remain framework-independent.

---

# Repository

Repositories manage persistence.

Responsibilities:

- CRUD operations.
- Database queries.
- Persistence.
- Transaction management.

Repositories must not:

- Implement business logic.
- Return HTTP responses.

---

# Schemas

Schemas define the API contract.

Responsibilities:

- Request models.
- Response models.
- Validation models.

Schemas should not contain business logic.

---

# Dependencies

Dependencies provide feature-specific dependency injection.

Only create dependencies that are actually required.

Avoid unnecessary dependency wrappers.

---

# Exceptions

Feature-specific exceptions belong inside the feature.

Shared exceptions belong under:

```text
app/exceptions/
```

Do not duplicate shared exceptions.

---

# Feature Registration

Every feature must be registered in two places.

## Feature Export

Update

```text
app/features/__init__.py
```

to expose the feature.

Example

```python
from . import users

__all__ = [
    "users",
]
```

---

## Router Registration

Register the feature router inside

```text
app/api/router.py
```

Example

```python
from app.features import users

api_router.include_router(users.router)
```

Route registration must always be explicit.

Do not use automatic route discovery.

---

# Database Models

Database models are shared across the application.

Create models under

```text
app/db/models/
```

Repositories should use these models.

Features should not define their own database models.

---

# Shared Functionality

Only move code into

```text
app/shared/
```

when it is reused across multiple features.

Feature-specific code should remain inside the feature.

---

# Feature Independence

Features should be loosely coupled.

Avoid direct dependencies between features whenever practical.

When interaction is required, prefer communication through services rather than accessing another feature's repository directly.

---

# Adding a New Feature

When creating a new feature:

1. Create the feature directory.
2. Generate the standard feature files.
3. Implement the router.
4. Implement the service.
5. Implement the repository.
6. Define request and response schemas.
7. Register the feature.
8. Register the router.
9. Add tests.

Every feature should follow the same workflow.

---

# Guiding Philosophy

Every feature should look familiar.

A developer should be able to navigate any feature without learning a different structure.

Consistency is more valuable than personal preference.

When in doubt:

- follow the standard feature structure
- keep responsibilities separated
- avoid unnecessary abstraction
- preserve consistency across the project