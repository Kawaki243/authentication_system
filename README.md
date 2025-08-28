# 🔐 Authentication System

## 📌 Overview
This authentication system is a secure, robust user management platform built with Java Spring Boot that provides comprehensive authentication and authorization features for web applications. The system implements industry-standard security practices including secure user registration, login functionality, password management, and role-based access control.

### 🛠️ Tech Stack
- **Backend:** ☕ Java, Spring Boot, Spring Security, Spring MVC, Spring Data JPA
- **Frontend:** 🎨 HTML, CSS, Bootstrap, JavaScript
- **Database:** 🗄️ MySQL
- **Build Tool:** 🔨 Maven
- **IDE:** 💻 Spring Tool Suite (STS)

## 🌟 Features

### 🔒 Core Authentication Features
- 🔑 **User Registration:** Secure user signup with email verification
- 🔐 **User Login/Logout:** Session-based authentication with secure logout
- 🛡️ **Password Security:** BCrypt encryption for secure password storage

### 👤 User Management
- 👨‍💼 **Profile Management:** View and update user profile information
- 📧 **Email Verification:** Confirm user email addresses
- ⏰ **Session Management:** Automatic session timeout and renewal


### 🔐 Security Features
- 🛡️ **CSRF Protection:** Cross-Site Request Forgery protection
- 🔒 **XSS Prevention:** Cross-Site Scripting attack prevention
- 🚪 **Role-Based Access Control (RBAC):** Fine-grained permission system
- 📝 **Audit Logging:** Track authentication events and user actions
- 🔄 **Token Management:** JWT or session-based token handling

## 🏗️ Application Architecture

### 📂 Project Structure
```
src/
├── main/
│   ├── java/
│   │   ├── config/          # Security and application configuration
│   │   ├── controller/      # REST controllers and web endpoints
│   │   ├── dto/            # Data Transfer Objects
│   │   ├── entity/         # JPA entity classes
│   │   ├── repository/     # Data access layer
│   │   ├── service/        # Business logic layer
│   │   └── util/          # Utility classes
│   └── resources/
│       ├── static/         # CSS, JS, images
│       ├── templates/      # Thymeleaf templates
│       └── application.properties
```

### 🔧 Key Components
- **🔐 SecurityConfig:** Spring Security configuration
- **👤 UserEntity:** User data model with roles and permissions  
- **🔑 AuthController:** Authentication endpoints (login, register, logout)
- **👨‍💼 UserService:** User management business logic
- **📧 EmailService:** Email verification and password reset
- **🛡️ JwtUtil:** JWT token generation and validation (if applicable)

## 🚀 Getting Started

### 📋 Prerequisites
- ☕ **Java Development Kit (JDK) 11+**
- 🔧 **Maven 3.6+**
- 🗄️ **MySQL 8.0+**
- 📧 **SMTP Server** (for email functionality)

### ⚙️ Installation Steps

#### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Kawaki243/authentication_system.git
cd authentication_system
```

#### 2️⃣ Database Setup
Create a MySQL database:
```sql
CREATE DATABASE auth_system;
CREATE USER 'auth_user'@'localhost' IDENTIFIED BY 'your_password';
GRANT ALL PRIVILEGES ON auth_system.* TO 'auth_user'@'localhost';
FLUSH PRIVILEGES;
```

#### 3️⃣ Configure Application Properties
Update `src/main/resources/application.properties`:
```properties
# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/auth_system
spring.datasource.username=auth_user
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

# Email Configuration (for password reset)
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=your_email@gmail.com
spring.mail.password=your_app_password
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

# JWT Configuration (if using JWT)
jwt.secret=your_jwt_secret_key
jwt.expiration=86400000

# Server Configuration
server.port=8080
```

#### 4️⃣ Build the Application
```bash
mvn clean install
```

#### 5️⃣ Run the Application
```bash
mvn spring-boot:run
```

#### 6️⃣ Access the Application
- **Main Application:** `http://localhost:8080/`
- **Login Page:** `http://localhost:8080/login`
- **Registration:** `http://localhost:8080/register`
## 📡 API Endpoints

### Authentication Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | User registration |
| POST | `/api/auth/login` | User login |
| POST | `/api/auth/logout` | User logout |
| GET | `/api/auth/verify-email` | Email verification |

### User Management Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/user/profile` | Get user profile |
| PUT | `/api/user/profile` | Update user profile |
| POST | `/api/user/change-password` | Change password |

### Admin Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/admin/users` | Get all users |
| GET | `/api/admin/users/{id}` | Get user by ID |
| PUT | `/api/admin/users/{id}` | Update user |
| DELETE | `/api/admin/users/{id}` | Delete user |

## 🔒 Security Implementation

### Password Security
- **BCrypt Hashing:** All passwords are encrypted using BCrypt
- **Strength Validation:** Enforces strong password policies
- **Reset Tokens:** Secure, time-limited password reset tokens

### Session Security
- **Session Timeout:** Automatic logout after inactivity
- **Secure Cookies:** HTTPOnly and Secure cookie flags
- **CSRF Tokens:** Protection against cross-site request forgery

## 🧪 Testing

### Run Tests
```bash
# Run all tests
mvn test

# Run specific test class
mvn test -Dtest=AuthControllerTest

# Run with coverage report
mvn test jacoco:report
```

## 📦 Deployment

### Production Configuration
1. Set production database credentials
2. Configure email service provider
3. Set secure JWT secret keys
4. Enable HTTPS/SSL certificates
5. Configure proper CORS settings

### Docker Deployment (Optional)
```dockerfile
FROM openjdk:11-jre-slim
COPY target/authentication-system-1.0.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/app.jar"]
```

## 🤝 Contributing
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Issues & Support
If you encounter any issues or have questions:
- 🐛 [Report a Bug](https://github.com/Kawaki243/authentication_system/issues)
- 💡 [Request a Feature](https://github.com/Kawaki243/authentication_system/issues)
- 📧 Contact: kawaki243@example.com

## 🙏 Acknowledgments
- Spring Boot community for excellent documentation
- Spring Security for robust security framework
- Contributors and testers

---

<h3 align="center">🔐 Secure Authentication Made Simple! 🚀</h3>
<p align="center">If you found this project helpful, <b>give it a star ⭐ on GitHub!</b> 😊</p>
