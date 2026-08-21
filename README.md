# Project LIBRA

A full-stack web-based library management system for managing book catalogs, user roles, borrowing and return transactions, loan availability, and library reports.

Built with Java, Spring Boot, Spring MVC, JPA/Hibernate, Thymeleaf, and MySQL using a layered MVC/N-tier architecture.

## Features

- Book catalog management, including book records, categories, genres, and synopses
- Book search, sorting, filtering, and unavailable-book handling
- Borrowing and return workflows with loan and availability management
- Role-based user administration and profile settings
- Library reports and operational record management
- Recommended-book displays and dynamic book cards
- Responsive web interfaces and borrow-confirmation workflows

## Tech Stack

| Area | Technologies |
|---|---|
| Backend | Java, Spring Boot, Spring MVC |
| Data Access | Spring Data JPA, Hibernate |
| Database | MySQL |
| Frontend | Thymeleaf, HTML, CSS, JavaScript |
| Architecture | Layered MVC / N-tier |
| Tools | Git, GitHub, Maven |

## Architecture

The application follows a layered MVC/N-tier architecture:

```text
Controller → Service → Repository → Database
```

- **Controllers** handle HTTP requests and route users to the appropriate views.
- **Services** contain application and business logic for books, borrowing, returns, users, and reports.
- **Repositories** manage data access through JPA/Hibernate.
- **Thymeleaf templates** render server-side web pages and user-facing interfaces.
- **MySQL** stores application data.

## Core Workflows

### Borrowing and returns

Users can browse available books and submit borrowing requests. The application manages loan status and availability so that books are not treated as available while actively borrowed. Return actions update the relevant loan and book records.

### Role-based administration

Administrative functions support user-role management and library operations. User-facing functionality includes book browsing, profile settings, and borrowing-related workflows.

### Book management

The system supports adding and updating book records, including categories, genres, synopses, availability, and filtering options.

## Getting Started

### Prerequisites

- Java 17 or later
- Maven
- MySQL
- An IDE such as IntelliJ IDEA

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   cd YOUR-REPOSITORY
   ```

2. Create a MySQL database:

   ```sql
   CREATE DATABASE libra_db;
   ```

3. Configure database credentials in:

   ```text
   src/main/resources/application.properties
   ```

   Example:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/libra_db
   spring.datasource.username=YOUR_USERNAME
   spring.datasource.password=YOUR_PASSWORD
   spring.jpa.hibernate.ddl-auto=update
   ```

4. Run the application:

   ```bash
   ./mvnw spring-boot:run
   ```

5. Open the application in your browser:

   ```text
   http://localhost:8080
   ```

## Project Context

Project LIBRA was developed as an academic software-engineering project. Development involved backend implementation, frontend integration, usability improvements, debugging, and GitHub-based collaboration.

## Contributors

- Chelsea Rose J. Pimentel — Full-Stack Developer (Backend-Focused)
- Add other team members and roles here

## License

This project was developed for academic purposes.
