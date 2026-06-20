# 🏦 Banking Portal

A secure and scalable Banking Management System built using **Spring Boot**, **Spring Security**, **JWT Authentication**, **Hibernate/JPA**, and **MySQL**. The application provides RESTful APIs for user account management, fund transfers, cash transactions, PIN management, and transaction tracking.

---

## 🚀 Project Overview

Banking Portal API is designed to simulate core banking operations while following industry-standard security practices. It enables users to securely manage their accounts, perform financial transactions, and view transaction history through authenticated API endpoints.

The project follows a layered architecture and demonstrates best practices in backend development using the Spring ecosystem.

---

## ✨ Key Features

### 👤 User Management

* User Registration
* User Authentication
* JWT-based Authorization
* Secure Password Encryption
* Profile Management

### 🔐 Security Features

* Spring Security Integration
* JWT Token Authentication
* Role-Based Access Control
* Secure API Endpoints
* Password Encryption using BCrypt

### 💳 Banking Operations

* Create Bank Account
* Account Information Retrieval
* Balance Inquiry
* Cash Deposit
* Cash Withdrawal
* Fund Transfer Between Accounts

### 🔑 PIN Management

* Create Transaction PIN
* Update PIN
* Secure PIN Validation

### 📊 Transaction Management

* Transaction History
* Fund Transfer Records
* Deposit Records
* Withdrawal Records
* Account Activity Tracking

### ⚠️ Exception Handling

* Global Exception Handling
* Validation Error Responses
* Account Not Found Handling
* Insufficient Balance Handling
* Unauthorized Access Handling

---

## 🛠️ Tech Stack

### Backend

* Java 17+
* Spring Boot
* Spring Security
* Spring Data JPA
* Hibernate
* JWT Authentication

### Database

* MySQL

### Build Tool

* Maven

### API Testing

* Postman
* Swagger/OpenAPI (Optional)

### Development Tools

* IntelliJ IDEA / Eclipse
* Git & GitHub

---

## 📂 Project Structure

```text
src
├── main
│   ├── java
│   │   ├── controller
│   │   ├── service
│   │   ├── repository
│   │   ├── entity
│   │   ├── dto
│   │   ├── security
│   │   ├── exception
│   │   └── config
│   └── resources
│       ├── application.properties
│       └── static
└── test
```

---

## 🔄 API Workflow

### User Registration

1. User submits registration details.
2. System validates user information.
3. Password is encrypted and stored.
4. Account is successfully created.

### Login Authentication

1. User submits credentials.
2. Credentials are validated.
3. JWT token is generated.
4. User receives access token.

### Fund Transfer

1. User enters recipient account details.
2. System verifies account validity.
3. Balance is checked.
4. Amount is transferred securely.
5. Transaction record is generated.

---

## 🗄️ Database Design

### Main Entities

#### User

* User ID
* Name
* Email
* Phone Number
* Address
* Password

#### Account

* Account Number
* Account Type
* Current Balance
* Account Status

#### Transaction

* Transaction ID
* Transaction Type
* Amount
* Timestamp
* Sender Account
* Receiver Account

#### PIN

* PIN ID
* Encrypted PIN
* User Association

---

## 📥 Installation & Setup

### Clone Repository

```bash
git clone https://github.com/your-username/BankingPortal-API.git
cd BankingPortal-API
```

### Configure Database

Create a MySQL database:

```sql
CREATE DATABASE banking_portal;
```

### Configure Application Properties

Create:

```properties
src/main/resources/application.properties
```

Add your database configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/banking_portal
spring.datasource.username=root
spring.datasource.password=password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

jwt.secret=your-secret-key
```

### Build Project

```bash
mvn clean install
```

### Run Application

```bash
mvn spring-boot:run
```

Application starts at:

```text
http://localhost:8080
```

---

## 🔑 Authentication

Protected APIs require a JWT token.

Example Header:

```http
Authorization: Bearer <jwt-token>
```

---

## 📌 Sample API Endpoints

### Authentication

| Method | Endpoint           | Description   |
| ------ | ------------------ | ------------- |
| POST   | /api/auth/register | Register User |
| POST   | /api/auth/login    | User Login    |

### Account

| Method | Endpoint             | Description         |
| ------ | -------------------- | ------------------- |
| GET    | /api/account/{id}    | Get Account Details |
| GET    | /api/account/balance | Check Balance       |

### Transactions

| Method | Endpoint                  | Description         |
| ------ | ------------------------- | ------------------- |
| POST   | /api/transaction/deposit  | Deposit Money       |
| POST   | /api/transaction/withdraw | Withdraw Money      |
| POST   | /api/transaction/transfer | Transfer Funds      |
| GET    | /api/transaction/history  | Transaction History |

### PIN

| Method | Endpoint        | Description |
| ------ | --------------- | ----------- |
| POST   | /api/pin/create | Create PIN  |
| PUT    | /api/pin/update | Update PIN  |

---

## 🧪 Testing

Use Postman to test APIs.

Example:

```http
POST /api/auth/login
```

Request Body:

```json
{
  "email": "user@gmail.com",
  "password": "password123"
}
```

---

## 🔮 Future Enhancements

* Email Notifications
* OTP Verification
* Two-Factor Authentication (2FA)
* Bank Statement Generation (PDF)
* Scheduled Transactions
* Dashboard Analytics
* Pagination & Filtering
* Docker Deployment
* CI/CD Integration
* Redis Caching
* Microservices Migration

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature/new-feature
```

3. Commit your changes

```bash
git commit -m "Add new feature"
```

4. Push to GitHub

```bash
git push origin feature/new-feature
```

5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Shubham Raj**

* MCA Student
* Java Full Stack Developer
* Spring Boot Enthusiast
* Open Source Contributor

---

⭐ If you found this project useful, please give it a Star on GitHub and support the project.
