# AIClass Assistant API

A Spring Boot REST API application designed to support student performance analysis and AI-powered educational assistance.

## 🚀 Project Overview

AIClass Assistant is a backend API built with Spring Boot that provides a foundation for educational technology applications. The application is designed to handle student data, performance metrics, and integrate with AI services to provide intelligent educational insights.

## 🛠️ Technology Stack

- **Java 21** - Latest LTS version
- **Spring Boot 3.5.5** - Modern Spring framework
- **Spring Data JPA** - Data persistence layer
- **Spring Web** - REST API endpoints
- **PostgreSQL** - Primary database
- **Lombok** - Code generation for boilerplate reduction
- **Maven** - Build and dependency management
- **Spring Boot DevTools** - Development productivity

## 📋 Prerequisites

Before running this application, make sure you have:

- **Java 21** installed (OpenJDK recommended)
- **Maven 3.6+** installed
- **PostgreSQL database** access
- **IDE** (IntelliJ IDEA, Eclipse, or VS Code recommended)

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone ethx42/student-performance-api
cd student-performance-api
```

### 2. Database Configuration

The application is configured to connect to a PostgreSQL database. Update the database connection settings in `src/main/resources/application.yml`:

```yaml
spring:
  datasource:
    url: jdbc:postgresql://your-database-host:5432/your-database-name
    username: your-username
    password: your-password
```

**Note:** The current configuration includes a Supabase PostgreSQL connection. Make sure to update these credentials with your own database settings.

### 3. Install Dependencies
```bash
./mvnw clean install
```

### 4. Run the Application
```bash
./mvnw spring-boot:run
```

The application will start on `http://localhost:8080`

## 🏗️ Project Structure

```
src/
├── main/
│   ├── java/
│   │   └── com/viveek/aiclass/
│   │       └── AiclassApplication.java     # Main application class
│   └── resources/
│       ├── application.yml                 # Main configuration
│       └── application.properties          # Additional properties
└── test/
    └── java/
        └── com/viveek/aiclass/
            └── AiclassApplicationTests.java # Test class
```

## 🔧 Configuration

### Application Properties

- **Server Port:** 8080 (configurable in `application.yml`)
- **Database:** PostgreSQL with JPA/Hibernate
- **JPA Settings:**
  - `ddl-auto: validate` - Validates database schema
  - `show-sql: true` - Enables SQL logging
  - Hibernate PostgreSQL dialect

### Environment Variables

For production deployment, consider using environment variables for sensitive configuration:

```bash
export SPRING_DATASOURCE_URL=jdbc:postgresql://host:port/database
export SPRING_DATASOURCE_USERNAME=username
export SPRING_DATASOURCE_PASSWORD=password
```

## 🧪 Testing

Run the test suite:
```bash
./mvnw test
```

## 📦 Building for Production

Create a production-ready JAR:
```bash
./mvnw clean package
```

Run the built JAR:
```bash
java -jar target/aiclass-0.0.1-SNAPSHOT.jar
```

## 🐳 Docker Deployment (Optional)

Create a `Dockerfile` for containerized deployment:
```dockerfile
FROM openjdk:21-jdk-slim
COPY target/aiclass-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/app.jar"]
```

## 🚀 Development Workflow

1. **Hot Reload:** Spring Boot DevTools is included for automatic restarts during development
2. **Database Changes:** Update schema and set `ddl-auto` appropriately
3. **API Development:** Add controllers, services, and repositories as needed
4. **Testing:** Write unit and integration tests for new features

## 📚 API Documentation

Currently, the application serves as a foundation. To add API documentation:

1. Add SpringDoc OpenAPI dependency
2. Configure Swagger UI
3. Document endpoints with annotations

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📋 TODO / Roadmap

- [ ] Add REST controllers for student management
- [ ] Implement performance analytics endpoints
- [ ] Add AI integration capabilities
- [ ] Implement authentication and authorization
- [ ] Add API documentation with Swagger
- [ ] Create database migration scripts
- [ ] Add comprehensive test coverage
- [ ] Implement caching layer
- [ ] Add monitoring and logging

## ⚠️ Security Notes

- Update database credentials before production deployment
- Implement proper authentication/authorization
- Use environment variables for sensitive configuration
- Enable HTTPS in production
- Regularly update dependencies for security patches

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Authors

- **Santiago Torres** - Initial development

## 🆘 Support

If you encounter any issues or have questions:

1. Check the existing issues in the repository
2. Create a new issue with detailed information
3. Contact the development team

---

**Happy Coding! 🎓💻**
