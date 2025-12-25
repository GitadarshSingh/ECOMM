# 🛒 Ecomm — Spring Boot E-Commerce Backend

![Java](https://img.shields.io/badge/Java-17+-red)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-Backend-brightgreen)
![MySQL](https://img.shields.io/badge/Database-MySQL%208-blue)
![Build](https://img.shields.io/badge/Build-Maven-orange)
![Status](https://img.shields.io/badge/Status-Active-success)

---

## 🚀 Overview

**Ecomm** is a modular, REST-driven Spring Boot backend for an e-commerce system.  
It handles **users, products, and orders**, backed by **MySQL**, following clean layered architecture (Controller → Service → Repository).

Designed for scalability, API clarity, and backend interview readiness.

---

## ✨ Core Features

### 👤 User Management
- User registration
- Secure login
- Fetch all users

### 📦 Product Management
- Add new products
- Fetch all products
- Fetch product by ID
- Delete products

### 🧾 Order Management
- Place orders for a user
- Fetch all orders
- Fetch orders by specific user

---

## 🛠 Tech Stack

| Layer        | Technology |
|--------------|------------|
| Language     | Java 17+ |
| Framework    | Spring Boot |
| ORM          | Spring Data JPA |
| Database     | MySQL 8 |
| Build Tool   | Maven |
| API Style    | REST |

---

## 📂 Project Structure

com.cfs.Ecomm
│
├── controller
│ ├── OrderController.java
│ ├── ProductController.java
│ └── UserController.java
│
├── dto
│ └── OrderDTO.java
│
├── model
│ ├── User.java
│ ├── Product.java
│ ├── Orders.java
│ └── OrderItem.java
│
├── repo
│ ├── UserRepository.java
│ ├── ProductRepository.java
│ └── OrderRepository.java
│
└── service
├── UserService.java
├── ProductService.java
└── OrderService.java

pgsql
Copy code

---

## 🗄 Database Configuration

📁 `src/main/resources/application.properties`

```properties
spring.application.name=Ecomm

spring.datasource.url=jdbc:mysql://localhost:3306/ecomDB
spring.datasource.username=root
spring.datasource.password=root
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.database-platform=org.hibernate.dialect.MySQL8Dialect
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
📌 Create database manually before running:

sql
Copy code
CREATE DATABASE ecomDB;
📌 REST API Endpoints
👤 Users
Method	Endpoint	Description
POST	/users/register	Register new user
POST	/users/login	Login user
GET	/users	Fetch all users

📦 Products
Method	Endpoint	Description
GET	/products	Fetch all products
GET	/products/{id}	Fetch product by ID
POST	/products	Add product
DELETE	/products/{id}	Delete product

🧾 Orders
Method	Endpoint	Description
POST	/orders/place/{userId}	Place order
GET	/orders/all-orders	Fetch all orders
GET	/orders/user/{userId}	Fetch user orders

⚡ How to Run
bash
Copy code
git clone https://github.com/<your-username>/Ecomm.git
cd Ecomm
mvn spring-boot:run
🔗 API Base URL:

arduino
Copy code
http://localhost:8080/
🧠 Architectural Highlights
Clean separation of concerns

DTO usage for request/response safety

JPA entity relationships

Production-ready REST conventions

Easy extension for JWT, Swagger, pagination

📈 Future Enhancements
JWT authentication & role-based access

Swagger / OpenAPI documentation

Pagination & filtering

Payment gateway integration

Dockerized deployment

⭐ Why This Project Matters
This project demonstrates:

Real-world backend design

Spring Boot proficiency

REST API structuring

Database integration skills

Interview-grade code organization
