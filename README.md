# Spring Boot JPA / Hibernate Course Project

A professional study project developed during a **JPA/Hibernate and Spring Boot** course.

This repository demonstrates how to build a layered REST API with **Spring Boot 4**, **Spring Data JPA**, and **Hibernate**, using an e-commerce-style domain to practice entity mapping, persistence, relationships, and CRUD operations.

## Overview

The application exposes REST endpoints for managing core resources such as:

- Users
- Orders
- Products
- Categories

It also includes examples of:

- One-to-many relationships
- Many-to-many relationships
- One-to-one relationships
- Composite keys with embedded IDs
- Enum persistence
- Exception handling in REST controllers
- Seed data for a test profile

## Tech Stack

- **Java 25**
- **Spring Boot 4.0.3**
- **Spring Data JPA**
- **Hibernate**
- **H2 Database** for local/test execution
- **PostgreSQL Driver** included for runtime usage
- **Maven Wrapper** for build and execution

## Architecture

The project follows a common layered backend structure:

- **Entities**: JPA domain models and relationship mappings
- **Repositories**: Spring Data JPA repositories
- **Services**: business logic and orchestration layer
- **Resources**: REST controllers / API endpoints
- **Configuration**: test profile bootstrap and database seeding

## Domain Model

The project models a simplified commerce scenario with the following main entities:

- `User`
- `Order`
- `OrderItem`
- `Payment`
- `Product`
- `Category`

### Relationships covered in the course project

- A **user** can have many **orders**
- An **order** can contain many **order items**
- A **product** can appear in many **order items**
- A **product** can belong to many **categories**
- An **order** can have one **payment**

This makes the repository a solid reference for practicing relational modeling with JPA/Hibernate.

## API Endpoints

Base URL when running locally:

```text
http://localhost:8080
```

### Users

- `GET /users`
- `GET /users/{id}`
- `POST /users`
- `PUT /users/{id}`
- `DELETE /users/{id}`

### Orders

- `GET /orders`
- `GET /orders/{id}`

### Products

- `GET /products`
- `GET /products/{id}`

### Categories

- `GET /categories`
- `GET /categories/{id}`

## Running the Project

### Prerequisites

Make sure you have installed:

- **Java 25**
- **Maven** (optional if using the wrapper)

### Start the application

Using the Maven Wrapper:

```bash
./mvnw spring-boot:run
```

Or build and run the JAR:

```bash
./mvnw clean package
java -jar target/course-0.0.1-SNAPSHOT.jar
```

## Database and Profiles

The default active profile is `test`, which uses an in-memory **H2** database.

Main test profile characteristics:

- In-memory database for quick local execution
- Automatic seed data loading at startup
- H2 console enabled
- SQL logging enabled

### H2 Console

When the application is running, the H2 console is available at:

```text
http://localhost:8080/h2-console
```

Default connection settings configured in the project:

- **JDBC URL:** `jdbc:h2:mem:testdb`
- **User:** `sa`
- **Password:** *(empty)*

## Sample Learning Topics Covered

This course project is useful for revisiting and demonstrating concepts such as:

- Object-relational mapping with JPA
- Entity associations and join tables
- Embedded composite primary keys
- RESTful resource design with Spring MVC
- Basic CRUD operations
- Service and repository separation
- Exception handling patterns in Spring Boot applications
- Test profile configuration and initial database seeding

## Project Structure

```text
src/
 ├── main/
 │   ├── java/com/educandoweb/course/
 │   │   ├── config/
 │   │   ├── entities/
 │   │   ├── repositories/
 │   │   ├── resources/
 │   │   └── services/
 │   └── resources/
 └── test/
```

## Why this repository matters

If you are studying **Spring Boot with JPA/Hibernate**, this repository can serve as:

- A portfolio-ready backend study project
- A reference for entity relationship mapping
- A base template for simple REST APIs
- A practical review of a course's most important concepts

- badges
- architecture diagram section
- sample JSON requests/responses
- deployment section
- bilingual version (English + Portuguese)
