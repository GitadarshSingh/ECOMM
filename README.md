Ecomm - Spring Boot E-commerce Application
Project Overview

Ecomm is a Spring Boot-based e-commerce backend application that provides APIs for managing users, products, and orders. It uses MySQL as the database and follows a RESTful architecture.

Features

User Management

Register new users

User login

List all users

Product Management

Add new products

Fetch all products

Fetch product by ID

Delete product

Order Management

Place an order for a user

Fetch all orders

Fetch orders by user

Technologies Used

Java 17+

Spring Boot

Spring Data JPA

MySQL 8

REST APIs

Maven

Project Structure
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

Database Configuration

Configured in application.properties:

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

API Endpoints
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
