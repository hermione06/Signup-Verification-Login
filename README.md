# UserManager

## Overview
This project is a complete Spring Boot application that implements secure signup, email verification, and login functionality. It uses Spring Security for authentication and password encryption, JWT for token-based authentication, and JavaMailSender for email verification.

## Features
1. **Secure Signup**
   - User registration with hashed passwords.
   - Input validation for user details (e.g., email format, password strength).

2. **Email Verification**
   - Sends a unique verification code to the user's email.
   - Resend optional available.
   - Token-based verification to activate user accounts.

3. **Login**
   - Email and password-based login.
   - Generates JWT tokens for stateless authentication.

4. **Additional Enhancements**
   - Password recovery option.
   - Role-based access control (optional).

## Technologies Used
- **Backend Framework**: Spring Boot
- **Authentication**: Spring Security, JWT
- **Database**: MySQL
- **Email Service**: JavaMailSender
- **Tools**: Gradle, JDK 23

## Prerequisites
- Java Development Kit (JDK 17 or higher)
- Gradle
- MySQL database setup

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/hermione06/Signup-Verification-Login.git
cd Signup-Verification-Login
```

### 2. Configure the Application
1. Open `application.properties`.
2. Set the following configurations:

```properties
# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/your_database
spring.datasource.username=your_username
spring.datasource.password=your_password

# Email Configuration
spring.mail.host=smtp.gmail.com #or smtp.mail.ru
spring.mail.port=587
spring.mail.username=your_email
spring.mail.password=your_email_password
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

# JWT Secret
jwt.secret=your_secret_key
jwt.expiration=86400000  # 1 day in milliseconds
```

### 3. Run the Application
```bash
gradle bootRun
```

The application will start on `http://localhost:8080` by default.

## API Endpoints - Screenshots
![register](https://github.com/user-attachments/assets/0300aa46-7765-4f91-be20-934d873b9a0c) ![email_code](https://github.com/user-attachments/assets/95235506-56af-421e-981c-558720942fa2) ![verify](https://github.com/user-attachments/assets/242ff7bf-fe40-44c1-9fab-215d0b60cf4c)

![login](https://github.com/user-attachments/assets/baa20967-147a-4960-afd2-67c027fced99)

## Security Features
1. **Password Hashing**: BCrypt hashing algorithm ensures secure storage of passwords.
2. **Token-Based Authentication**: JWT tokens provide secure and stateless authentication mechanism.
3. **Email Verification**: Users must verify their email before accessing their account.


## Testing
- Use **Postman** or similar tools to test the APIs.

## Future Enhancements
- Implement password recovery.
- Add two-factor authentication (2FA).

## License
This project is licensed under the MIT License.

## Contributors
- [Asiman Ismayilova](https://github.com/hermione06)

---
Feel free to contribute by submitting issues or pull requests!

