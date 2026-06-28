---
trigger: model_decision
description: Load when beginning a new engineering session or when a comprehensive understanding of the repository is required before implementation or review.
---

# Repository Indexing Playbook

## Purpose

The purpose of repository indexing is to build an internal understanding of the codebase before performing engineering work.

The objective is to minimize repeated repository exploration while ensuring future recommendations and implementations remain consistent with the existing project.

Repository indexing is an analysis activity.

It must never modify the repository.

---

# Objective

Build a comprehensive mental model of the repository.

This understanding should be reused throughout the current session.

Only revisit repository areas when:

- new evidence becomes available
- repository changes occur
- additional information is required

---

# Repository Index

The repository index should include the following information.

## Project Overview

Understand:

- project purpose
- application type
- major responsibilities
- deployment model

---

## Technology Stack

Identify:

- languages
- frameworks
- libraries
- build tools
- package managers
- databases
- infrastructure
- deployment technologies

---

## Repository Structure

Identify:

- top-level folders
- major modules
- application boundaries
- shared packages
- configuration locations

Produce a mental map of the repository.

---

## Architecture

Determine:

- architectural style
- layering
- dependency direction
- module relationships
- extension points

Avoid making assumptions.

---

## Coding Conventions

Identify repository conventions including:

- naming
- folder organization
- imports
- exports
- typing
- logging
- validation
- documentation

Treat repository conventions as authoritative.

---

## Existing Patterns

Identify recurring implementation patterns.

Examples:

- CRUD
- services
- dependency injection
- middleware
- routing
- data access
- state management
- error handling
- configuration

Future work should follow these patterns.

---

## Shared Components

Identify reusable:

- services
- utilities
- helpers
- abstractions
- components
- middleware
- libraries

Avoid duplicating functionality.

---

## External Integrations

Identify:

- APIs
- databases
- cloud services
- storage
- authentication
- third-party integrations

Understand how they interact with the application.

---

## Configuration

Identify:

- environment variables
- configuration files
- secrets handling
- deployment configuration

Do not expose secrets.

Only understand how configuration is organized.

---

## Runtime Behaviour

Understand:

- application startup
- request flow
- background processing
- scheduled tasks
- data flow

---

## Deployment

Understand:

- build process
- deployment process
- runtime environment
- infrastructure
- CI/CD pipeline

---

## Documentation

Locate and understand existing documentation.

Examples:

- architecture
- ADRs
- deployment
- API documentation
- contribution guides

Treat documentation as supporting evidence.

---

# Repository Constraints

Identify constraints such as:

- architectural boundaries
- technology choices
- coding standards
- deployment limitations
- performance considerations

Future recommendations should respect these constraints.

---

# Output

After indexing, provide a concise summary including:

- repository purpose
- architecture
- technology stack
- major modules
- implementation patterns
- reusable components
- deployment architecture
- important constraints

Do not produce an exhaustive report.

Summarize only the information necessary to establish repository context.

---

# Retention

Maintain the repository index throughout the current session.

Future engineering work should build upon this understanding instead of repeatedly re-analyzing unchanged areas.

Only update the repository index when new evidence is introduced.

---

# Completion Criteria

Repository indexing is complete when:

- the repository structure is understood
- architecture has been identified
- major modules are understood
- implementation patterns are recognized
- technology stack has been identified
- deployment architecture is understood
- repository conventions have been identified
- reusable components have been catalogued
- project constraints have been identified

Do not perform implementation during repository indexing.