# Ecommerce Project

## 📌 Overview

This is a simple E-commerce application built using **Spring Boot and Java**. The project demonstrates CRUD operations, authentication, and database integration.

## Technologies Used

- **Backend:** Spring Boot, Java
- **Database:** MySQL
- **Version Control:** Git & GitHub

Database Setup & Connectivity
The project uses **MySQL** as the database. Follow these steps to set it up and connect:

### 1️⃣ Ensure MySQL is Installed & Running
Make sure MySQL Server is installed and running on your system.

### 2️⃣ Create the Database Using the Provided SQL File
Run the following command in the terminal (Command Prompt, Git Bash, or MySQL Shell):

```sh
mysql -u root -p < amit_ecommerce_db.sql
```
This will:
✔️ Create the database (`amit_ecommerce_db`)
✔️ Import all necessary tables and data

Alternatively, if you want to manually create the database before importing:

```sql
CREATE DATABASE amit_ecommerce_db;
USE amit_ecommerce_db;
SOURCE amit_ecommerce_db.sql;
```

### 3️⃣ Update Database Credentials in `application.properties`
Modify the database configuration in your Spring Boot project:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/amit_ecommerce_db
spring.datasource.username=root
spring.datasource.password=MySQL@Amit3110
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
```

### 4️⃣ Run the Project
Once the database is set up, start the application(in CMD or Git Bash):

```sh
mvn spring-boot:run
```

Now, your project is successfully connected to MySQL and ready to go

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

