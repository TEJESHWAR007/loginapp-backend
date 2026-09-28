# Secure Login System - Backend

Spring Boot REST API for the Secure Login System featuring JWT authentication, Spring Security, and MySQL database integration.

## Tech Stack
- Java 17+ / 21
- Spring Boot 3.3+
- Spring Security 6 (Stateless JWT Filter)
- Spring Data JPA / Hibernate
- MySQL 8+
- JJWT (JSON Web Token)

## Prerequisites
- Java 17 or higher
- MySQL Server 8+
- Maven (or use included `./mvnw`)

## Database Setup
1. Start MySQL server.
2. Create the database using the script in `sql/init-db.sql` or run:
   ```sql
   CREATE DATABASE IF NOT EXISTS jwtauthdb;
   ```
3. Update database credentials in `src/main/resources/application.properties` if different from defaults.

## Running the Application

Using Maven wrapper:
- **Windows**:
  ```powershell
  .\mvnw.cmd spring-boot:run
  ```
- **Linux / macOS**:
  ```bash
  ./mvnw spring-boot:run
  ```

The server starts by default on `http://localhost:8081`.

## API Endpoints

| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| POST | `/api/auth/register` | Register a new user | No |
| POST | `/api/auth/login` | Log in and receive JWT token | No |
| GET | `/api/users/me` | Fetch authenticated user profile | Yes (Bearer Token) |

## Running Tests
```bash
.\mvnw.cmd test
```
