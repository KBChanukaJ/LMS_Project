# Learning Management System (LMS) - Backend

A robust and scalable backend service for a Learning Management System (LMS) built with **Spring Boot**. This REST API powers core educational features like user management, course delivery, assessments, and progress tracking.

---

## 🚀 Technology Stack

- **Framework:** Spring Boot 3.x
- **Language:** Java 17+
- **Database:** MySQL 8.x
- **Authentication:** JWT (JSON Web Tokens)
- **API Documentation:** Springdoc OpenAPI (Swagger UI)
- **Build Tool:** Maven
- **Testing:** JUnit 5, Mockito, Testcontainers (optional)

---

## 📋 Prerequisites

Before running this application, ensure you have the following installed on your machine:

- **JDK 17** or higher
- **Maven 3.6** or higher
- **MySQL 8.0** or higher
- **Git**

---

## ⚙️ Installation & Setup

Follow these steps to get the development environment running:

1.  **Clone the Repository**
    ```bash
    git clone <your-repository-url>
    cd lms-backend
    ```

2.  **Configure Database**
    - Create a new MySQL database named `lms_db`.
    - Update the database connection settings in `src/main/resources/application.properties` with your credentials.

3.  **Build the Project**
    ```bash
    mvn clean install
    ```

4.  **Run the Application**
    ```bash
    mvn spring-boot:run
    ```
    The application will start on `http://localhost:8080`.

---

## 🔧 Configuration

The main configuration file is `src/main/resources/application.properties`. Key configuration options:

```properties
# Server Port
server.port=8080

# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/lms_db?useSSL=false&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=your_password

# JPA Hibernate Properties
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
spring.jpa.show-sql=true

# JWT Secret (Change this in production!)
jwt.secret=your_very_strong_secret_key_here
jwt.expiration.ms=86400000 # 24 hours
