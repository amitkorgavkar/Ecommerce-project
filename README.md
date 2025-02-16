# Ecommerce Project

## 📌 Overview

This is a simple E-commerce application built using **Spring Boot and Java**. The project demonstrates CRUD operations, authentication, and database integration.

## Technologies Used

- **Backend:** Spring Boot, Java
- **Database:** MySQL
- **Version Control:** Git & GitHub

## How to Run the Project

1. Clone the repository:
   
   git clone https://github.com/amitkorgavkar/Ecommerce-project.git
   
2. Navigate to the project directory:
   
   cd Ecommerce-project
   
3. Build and run the project:
   
   mvn spring-boot:run
   
4. The server will start on:
   
   http://localhost:8080


## Directory Structure

Ecommerce-project/
│── src/
│   ├── main/
│   │   ├── java/com/example/ecommerce/  # Java source files
│   │   ├── resources/  # Configuration files (application.properties)
│   ├── test/
│── pom.xml  # Maven dependencies
│── README.md  # Project documentation

## 📌 API Endpoints

| Method | Endpoint         | Description            |
| ------ | ---------------- | ---------------------- |
| GET    | `/products`      | Fetch all products     |
| POST   | `/products`      | Add a new product      |
| PUT    | `/products/{id}` | Update product details |
| DELETE | `/products/{id}` | Remove a product       |

## DB Design

- **Tables:**
  - `Users (id, name, email, password, role)`
  - `Products (id, name, price, description, stock)`
  - `Orders (id, user_id, product_id, quantity, status)`

