# skb-bazar
🛒 E-Commerce Backend (Spring Boot + PostgreSQL)

A production-grade E-Commerce Backend built with Java 17, Spring Boot 3, PostgreSQL, JWT Authentication, Global Layer Architecture, and industry-standard backend practices.

📌 Features
User Authentication (JWT)
Role-based Authorization (Admin, Seller, Customer)
Products & Categories
Cart & Wishlist
Orders & Payments Ready Structure
Inventory Handling Structure
Global Exception Handling
DTO + Mapper Pattern
Logging (AOP + Logback)
Swagger API Documentation
Profiles: dev & prod
Database Versioning (Flyway)
Docker Ready Structure
Clean Folder Structure

🏗️ Architecture — Global Layer Architecture
Controller → Service → Repository → Entity
           ↓
       DTO + Mapper
           ↓
       Config Layer
           ↓
       Exception Layer + AOP Logging


This architecture ensures:-

Clean separation of concerns
Easy maintenance
Testable business logic
Scalability for new modules

📁 Folder Structure
project-root/
│── README.md
│── pom.xml
│── docker/
│── docs/
│── src/
│   ├── main/java/com/ecommerce/
│   │   ├── controller/        # REST Controllers
│   │   ├── service/           # Service Layer
│   │   ├── repository/        # Spring Data JPA Repos
│   │   ├── entity/            # JPA Entities
│   │   ├── dto/               # Data Transfer Objects
│   │   ├── mapper/            # Entity <-> DTO mappers
│   │   ├── config/            # Security, Swagger, CORS, etc.
│   │   ├── exception/         # Global exception handler
│   │   ├── aop/               # Logging AOP
│   │   └── util/              # Common utilities
│   └── main/resources/
│       ├── application.yml
│       ├── application-dev.yml
│       ├── application-prod.yml
│       ├── logback-spring.xml
│       └── db/migration/      # Flyway scripts
└── test/

⚙️ Configuration (Profiles)
application.yml
spring:
  profiles:
    active: dev

application-dev.yml

PostgreSQL local connection
Hibernate ddl-auto=update
Swagger enabled
Local logging
application-prod.yml
Production DB
Hibernate ddl-auto=validate
JSON logging

Enhanced security
🔐 Authentication (JWT)
Login → return Access + Refresh Token
Role-based APIs
Password hashing using BCrypt
Refresh token endpoint
Common response model

📦 Modules (Ready Structure)
✔ User Module
Authentication, Authorization, Roles

✔ Product Module
Product CRUD, Category CRUD, Images, Pagination

✔ Cart Module
Add/remove items, price calculation

✔ Wishlist Module
User-level wishlist management

✔ Order Module (Structure Ready)
Checkout flow, item list, address, summary

✔ Payment Integration (Structure Ready)
Supports Razorpay/Stripe integration

✔ Inventory Module (Structure Ready)
Stock management and validation

📚 API Documentation (Swagger)

Available at:
/swagger-ui.html

🧪 Run the Application
1. Clone
git clone [https://github.com/yourname/ecommerce-backend.git](https://github.com/sumitkprasad123/skb-bazar.git)
cd ecommerce-backend

2. Create Database
CREATE DATABASE ecommerce;

3. Run
mvn spring-boot:run

🧰 Technologies Used

Java 17
Spring Boot 3
PostgreSQL
Spring Security + JWT
Hibernate
Flyway
Logback
Maven
Docker (Optional)

👤 Author
sumitkprasad123

Backend Developer — Java, Spring Boot, PostgreSQL, kafka

