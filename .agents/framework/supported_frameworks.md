# Supported Frameworks

## Purpose

This document lists the application frameworks currently supported by the AI Skills Rules framework.

Each supported framework provides a standardized architecture, project structure, and implementation guidance to ensure projects are generated and maintained consistently.

Framework-specific knowledge is intentionally separated from the core engineering rules so that new frameworks can be added without changing the overall workflow.

---

# Current Support

## Backend Frameworks

### FastAPI

Status

- Supported

Project Bootstrap

- Supported

Feature Generation

- Supported

Framework Knowledge

```text
knowledge/
└── frameworks/
    └── fastapi/
        ├── architecture.md
        ├── boilerplate.md
        └── feature_structure.md
```

Capabilities

- Production-ready project scaffolding
- Feature-first architecture
- Standardized project structure
- Explicit route registration
- Repository pattern
- Service layer
- SQLAlchemy integration
- Alembic integration
- Docker support
- Testing structure
- Development tooling

---

# Planned Support

The following frameworks are planned for future releases.

## Backend

- Flask
- Django
- Express.js
- NestJS
- Go Fiber

## Frontend

- Next.js
- React
- Angular
- Vue.js
- SvelteKit

---

# Framework Selection

When bootstrapping a new project:

1. Identify the requested technology stack.
2. Select the appropriate framework.
3. Load the framework knowledge.
4. Generate the project using that framework's architecture.
5. Transition to the standard engineering workflow after project creation.

Framework selection occurs only during project bootstrap.

Once a project has been created, framework selection should not change unless explicitly requested by the developer.

---

# Framework Knowledge Structure

Every supported framework should provide the same knowledge structure.

```text
knowledge/
└── frameworks/
    └── <framework>/
        ├── architecture.md
        ├── boilerplate.md
        └── feature_structure.md
```

## architecture.md

Defines the recommended application architecture.

## boilerplate.md

Defines the standard project scaffold.

## feature_structure.md

Defines how new features should be organized and implemented.

This structure should remain consistent across all supported frameworks.

---

# Design Principles

Framework support should follow these principles.

- One architecture per framework.
- Consistent project organization.
- Minimal framework-specific assumptions.
- Reuse the shared engineering workflow.
- Keep framework knowledge isolated from generic engineering rules.

---

# Future Expansion

When adding support for a new framework:

- Add a new framework directory under `knowledge/frameworks/`.
- Implement the standard knowledge documents.
- Reuse the existing engineering rules.
- Reuse the existing playbooks whenever possible.
- Update this document to include the newly supported framework.

The objective is to expand framework support without introducing framework-specific behavior into the core AI engineering framework.