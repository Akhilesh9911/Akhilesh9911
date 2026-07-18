# 💻 Code Best Practices & Implementation Examples

Production-grade code examples demonstrating quality, security, and scalability.

---

## 🏗️ Project Structure Best Practices

### Recommended Spring Boot Project Structure
```
src/
├── main/
│   ├── java/com/hireforge/
│   │   ├── controller/
│   │   ├── service/
│   │   ├── repository/
│   │   ├── entity/
│   │   ├── dto/
│   │   ├── exception/
│   │   └── security/
│   └── resources/
│       ├── application.yml
│       ├── application-dev.yml
│       └── application-prod.yml
└── test/
    └── java/com/hireforge/
```

---

## 🔐 Security Implementation

### Spring Security with JWT
- Authentication via JWT tokens
- Role-based access control (RBAC)
- Password hashing with BCrypt
- Input validation & sanitization
- CORS configuration
- Rate limiting

### Best Practices Implemented
✅ Stateless authentication (JWT)
✅ Secure password storage (BCrypt)
✅ CORS properly configured
✅ Input validation on all endpoints
✅ Exception handling with error codes
✅ Logging for security events

---

## 📊 Database Design

### Key Principles
- Proper indexing on frequently queried columns
- Foreign keys for referential integrity
- NOT NULL constraints where appropriate
- Unique constraints for unique fields
- Normalized schema (3NF)
- Timestamp tracking (created_at, updated_at)

### Entity Relationships
- User → Resumes (1:N)
- User → JobApplications (1:N)
- User → Interviews (1:N)
- Proper cascade operations

### Query Optimization
- Pagination for large datasets
- Lazy loading for related entities
- Caching for frequently accessed data
- Batch processing for bulk operations

---

## 🛡️ Exception Handling

### Global Exception Handler
- Centralized exception handling
- Consistent error response format
- HTTP status codes properly mapped
- Validation errors clearly reported
- Logging for debugging

### Standard Error Response
```json
{
  "success": false,
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Clear error message",
    "status": 400,
    "timestamp": "2026-07-18T10:30:00Z"
  }
}
```

---

## 🔄 Service Layer

### Design Patterns Used
- Single Responsibility Principle
- Dependency Injection
- Service-Repository pattern
- Transaction management
- Business logic centralization

### Features
✅ Transactional operations
✅ Proper validation
✅ Clean separation of concerns
✅ Error handling
✅ Logging at appropriate levels

---

## 📝 REST Controller

### Best Practices
- Proper HTTP methods (GET, POST, PUT, DELETE)
- Correct status codes (200, 201, 400, 404, 500)
- Request/Response validation
- Authentication checks
- Pagination support
- Error handling

### API Response Format
```json
{
  "success": true,
  "message": "Operation successful",
  "data": { "content": "here" },
  "pagination": {
    "totalElements": 100,
    "totalPages": 10,
    "currentPage": 1
  }
}
```

---

## 🧪 Testing Strategy

### Unit Tests
- Service layer tests
- Repository layer tests
- DTO validation tests
- Util method tests

### Integration Tests
- API endpoint tests
- Database integration tests
- Security filter tests

### Test Coverage
- Target: 80%+ code coverage
- Focus on critical business logic
- Edge case testing

---

## 📦 DTO (Data Transfer Object)

### Request DTOs
- Input validation annotations
- Size constraints
- Email validation
- Required field checks

### Response DTOs
- Only necessary fields included
- Consistent naming conventions
- Builder pattern for construction
- Immutable where possible

---

## 🐳 Docker Best Practices

### Multi-stage Builds
- Separate build and runtime stages
- Minimal final image size
- Non-root user execution
- Health checks

### Example Dockerfile
```dockerfile
FROM maven:3.8-openjdk-17 as builder
WORKDIR /app
COPY pom.xml .
RUN mvn dependency:go-offline
COPY src ./src
RUN mvn clean package -DskipTests

FROM openjdk:17-slim
WORKDIR /app
RUN useradd -m -u 1000 appuser
COPY --from=builder /app/target/*.jar app.jar
RUN chown -R appuser:appuser /app
USER appuser
EXPOSE 8080
ENV JAVA_OPTS="-Xmx512m -Xms256m"
ENTRYPOINT ["java", "$JAVA_OPTS", "-jar", "app.jar"]
```

---

## 📝 Logging Best Practices

### Log Levels Used
- **DEBUG:** Detailed diagnostic information
- **INFO:** General informational messages
- **WARN:** Warning messages for potential issues
- **ERROR:** Error messages for exceptions

### What Gets Logged
✅ Business operations
✅ Security events
✅ Performance metrics
✅ Errors and exceptions
✅ API requests (non-sensitive)

### Sensitive Data
❌ Never log passwords
❌ Never log credit card numbers
❌ Never log personal tokens
✅ Log masked or hashed versions if needed

---

## 🚀 Performance Optimization

### Database
- Indexed frequently queried columns
- Query optimization
- Connection pooling (HikariCP)
- Pagination implementation

### Caching
- @Cacheable for read operations
- Cache invalidation strategy
- Redis for distributed caching

### API
- Response compression
- Pagination for large datasets
- Batch processing
- Async operations where needed

---

## ✅ Code Quality Checklist

- [ ] Follows SOLID principles
- [ ] DRY (Don't Repeat Yourself)
- [ ] Clear naming conventions
- [ ] Proper error handling
- [ ] Security best practices
- [ ] Performance optimized
- [ ] Tested thoroughly
- [ ] Well documented
- [ ] Scalable architecture
- [ ] Maintainable code

---

## 🎯 Key Takeaways

1. **Security First** - Authentication, authorization, validation
2. **Clean Code** - Readable, maintainable, follows patterns
3. **Scalability** - Designed for growth, proper indexing
4. **Testing** - Comprehensive test coverage
5. **Documentation** - Code comments, API docs
6. **Performance** - Optimized queries, caching
7. **Monitoring** - Logging, health checks
8. **DevOps** - Docker, CI/CD ready

---

**Last Updated:** July 2026 | Status: Production Quality ✅
