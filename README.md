# Restricted File Sharing System

This is a secure file sharing system built with Spring Boot. It allows users to register, login, verify their accounts, upload files, download files, and share files with other registered users.

## Features

- **User Authentication:**
  - User registration with email verification.
  - Secure login with JWT-based authentication.
- **File Management:**
  - Upload files securely.
  - Download files using a secure token.
  - Share files with other users.
  - View a list of your uploaded files.

## Technologies Used

- **Backend:**
  - Java 25
  - Spring Boot 4.0.2
  - Spring Security
  - Spring Data JPA
  - MySQL
  - Flyway
  - JJWT (Java JWT)
  - Lombok
- **Testing:**
  - JUnit 5
  - Spring Boot Test

## Getting Started

### Prerequisites

- Java 25
- Gradle
- MySQL

### Installation & Running

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/Restricted-File-Sharing-System.git
   ```
2. **Navigate to the `Authentication` directory:**
   ```bash
   cd Restricted-File-Sharing-System/Authentication
   ```
3. **Configure the database:**
   - Open `src/main/resources/application.yaml` and update the database configuration with your MySQL credentials.
4. **Build the project:**
   ```bash
   ./gradlew build
   ```
5. **Run the application:**
   ```bash
   ./gradlew bootRun
   ```
The application will be running at `http://localhost:8080`.

## API Endpoints

### Authentication

- `POST /api/auth/register`: Register a new user.
- `POST /api/auth/login`: Login to get a JWT token.
- `GET /api/verify?token={token}`: Verify user account.

### File Management

- `POST /api/files/upload`: Upload a file.
- `GET /api/files/download/{token}`: Download a file.
- `POST /api/files/share`: Share a file with other users.
- `GET /api/files/mine`: Get a list of files uploaded by the current user.
