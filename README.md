Ecomm - Spring Boot E-commerce Application

🚀 Project Overview

Ecomm is a Spring Boot-based backend for an e-commerce application.
It provides RESTful APIs to manage users, products, and orders, with MySQL as the database.

✨ Features
User Management

Register new users

User login

List all users

Product Management

Add new products

Retrieve all products or by ID

Delete products

Order Management

Place orders for a user

Retrieve all orders

Retrieve orders by user

🛠 Technologies Used

Java 17+

Spring Boot

Spring Data JPA

MySQL 8

Maven

REST APIs




📂 Project Structure
com.cfs.Ecomm
├── controller
│   ├── OrderController.java
│   ├── ProductController.java
│   └── UserController.java
├── dto
│   └── OrderDTO.java
├── model
│   ├── User.java
│   ├── Product.java
│   ├── Orders.java
│   └── OrderItem.java
├── repo
│   ├── UserRepository.java
│   ├── ProductRepository.java
│   └── OrderRepository.java
└── service
    ├── UserService.java
    ├── ProductService.java
    └── OrderService.java

    



🗄 Database Configuration

Located in src/main/resources/application.properties:

spring.application.name=Ecomm

spring.datasource.url=jdbc:mysql://localhost:3306/ecomDB
spring.datasource.username=root
spring.datasource.password=root
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.database-platform=org.hibernate.dialect.MySQL8Dialect
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true


Create the database before running:

CREATE DATABASE ecomDB;

📌 API Endpoints
Users
Method	Endpoint	Description
POST	/users/register	Register a new user
POST	/users/login	Login with email & password
GET	/users	Get all users
Products
Method	Endpoint	Description
GET	/products	Get all products
GET	/products/{id}	Get product by ID
POST	/products	Add a new product
DELETE	/products/{id}	Delete a product
Orders
Method	Endpoint	Description
POST	/orders/place/{userId}	Place an order
GET	/orders/all-orders	Get all orders
GET	/orders/user/{userId}	Get orders by user
⚡ How to Run

Clone the repository:

git clone https://github.com/<username>/Ecomm.git


Navigate to the project directory:

cd Ecomm


Build and run the Spring Boot application:

mvn spring-boot:run


Access APIs at:

http://localhost:8080/
